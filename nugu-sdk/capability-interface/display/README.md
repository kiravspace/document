---
description: Play 에서 전달하는 UI 요소를 화면에 구성하기 규격
---

# Display

## Version

최신 버전은 1.7 입니다.

| Version | Date | Description |
| :--- | :--- | :--- |
| 1.0 | 2019.11.17 | 규격 추가 |
| 1.1 | 2019.12.09 | Close directive CloseSucceeded, CloseFailed event 추가 Weather1/2/3/4/5, FullImage directive 추가 |
| 1.2 | 2020.03.03 | Duration 추가 Score1/2 directive 추가 ControlFocus, ControlScroll directive 추가 ControlFocusSucceeded, ControlFocusFailed, ControlScrollSucceeded, ControlScrollFailed event 추가 SearchList1/2 directive 추가 Call1/2/3 directive 추가 FullText3 directive 추가 |
| 1.3 | 2020.04.29 | Timer directive 추가 Template 에 supportFocusedItemToken, supportVisibleTokenList 필드 추가 |
| 1.4 | 2020.06.22 | ButtonObject 에 postback, autoTrigger, closeTemplateAfter, disable 필드 추가 ElementSelected event 에 postback 필드 추가 Dummy directive 추가 |
| 1.5 | 2020.09.02 | Template 에 eventType, textInput 필드 추가 |
| 1.6 | 2020.10.16 | BadgeObject, UnifiedSearch1 추가 |
| 1.7 | 2021.05.31 | StyleGrammarGuide, FloatingBannerObject 추가 |

## SDK Interface

### DisplayAgent 사용

Display interface 규격에 따른 디바이스의 동작 제어는 DisplayAgent 가 처리합니다.

{% tabs %}
{% tab title="Android" %}
NuguAndroidClient instance 를 통해 DisplayAgent instance 에 접근할 수 있습니다.

```text
val displayAgent = nuguAndroidClient.displayAgent
```

AudioPlayer interface 와 Display interface 를 병합해주는 DisplayAggregatorInterface 를 제공합니다.

```text
val displayAggregator = nuguAndroidClient.getDisplay()
```
{% endtab %}

{% tab title="iOS" %}
NuguClient instance 를 통해 DisplayAgent instance 에 접근할 수 있습니다.

```text
let audioPlayerAgent = nuguClient.audioPlayerAgent
```
{% endtab %}
{% endtabs %}

### Context 구성

[UI 제어](./#ui-1) 기능을 사용하기 위해서는 template 화면의 상태 정보를 [Context](./#context) 에 포함시켜 주어야 합니다.

{% tabs %}
{% tab title="Android" %}
DisplayAggregatorInterface.Controller 를 추가합니다.

```text
val controller = object: DisplayAggregatorInterface.Controller {
    override fun getFocusedItemToken(): String? {
        ...
    }

    override fun getVisibleTokenList(): List<String>? {
        ...
    }

    ...
}

displayAggregator.displayCardRendered(templateId, controller)
```
{% endtab %}

{% tab title="iOS" %}
DisplayAgentDelegate 를 추가합니다.

```text
class MyDisplayAgentDelegate: DisplayAgentDelegate {
    func displayAgentRequestContext(templateId: String, completion: @escaping (DisplayContext?) -> Void) {
        ...
    }

    ...
}
displayAgent.delegate = MyDisplayAgentDelegate()
```
{% endtab %}
{% endtabs %}

### UI 구성 및 제어

Display 로 화면을 구성하기 위해 필요한 데이터는 [Template](./#directive-template) directive 에 포함되어 전달됩니다.

Template 화면은 [Close](./#close) directive 또는 SDK 내부 timer 등에 의해 종료될 수 있으며, [Update](./#update) directive 에 의해 변경될 수 있습니다.

Template 의 focus 와 scroll 은 `사용자 발화` 에 따라 [ControlFocus](display-directive.md#controlfocus), [ControlScroll](display-directive.md#controlscroll) directive 로 제어될 수 있습니다.

{% tabs %}
{% tab title="Android" %}
DisplayAggregatorInterface.Renderer 를 추가합니다.

```text
val renderer = object: DisplayAggregatorInterface.Renderer {
    override fun render(templateId: String, templateType: String, templateContent: String, dialogRequestId: String, displayType: Type): Boolean {
        ...
    }

    ...
}
displayAggregator.setRenderer(renderer)
```

UI 를 제어하려면 DisplayAggregatorInterface.Controller 를 추가합니다.

```text
val controller = object: DisplayAggregatorInterface.Controller {
    override fun controlFocus(direction: Direction): Boolean {
        ...
    }

    override fun controlScroll(direction: Direction): Boolean {
        ...
    }

    ...
}
displayAggregator.displayCardRendered(templateId, controller)
```
{% endtab %}

{% tab title="iOS" %}
DisplayAgentDelegate 를 추가합니다.

```text
class MyDisplayAgentDelegate: DisplayAgentDelegate {
    func displayAgentShouldRender(template: DisplayTemplate, completion: @escaping (AnyObject?) -> Void) {
        ...
    }

    func displayAgentShouldMoveFocus(templateId: String, direction: DisplayControlPayload.Direction, completion: @escaping (Bool) -> Void) {
        ...
    }

    func displayAgentShouldScroll(templateId: String, direction: DisplayControlPayload.Direction, completion: @escaping (Bool) -> Void) {
        ...
    }

    ...
}
displayAgent.delegate = MyDisplayAgentDelegate()
```
{% endtab %}
{% endtabs %}

### 사용자 인터렉션 처리

Template 하위 항목 선택시 [ElementSelected](display-event.md#elementselected) event 가 전달됩니다.

{% tabs %}
{% tab title="Android" %}
```text
displayAggregator.setElementSelected(templateId, token, postback)
```
{% endtab %}

{% tab title="iOS" %}
```text
displayAgent.elementDidSelect(templateId: displayTemplate.templateId, token: token, postback: postback)
```
{% endtab %}
{% endtabs %}

Template 에 화면에 대한 사용자 interaction 발생시 SDK 로 notify 해주어야 내부 timer\(template 일정시간 노출 후 종료하기 위한\) 가 갱신됩니다.

{% tabs %}
{% tab title="Android" %}
```text
displayAggregator.notifyUserInteraction(templateId)
```
{% endtab %}

{% tab title="iOS" %}
```text
displayAgent.notifyUserInteraction()
```
{% endtab %}
{% endtabs %}

## Context

```text
{
  "Display": {
    "version": "1.7",
    "playServiceId": "{{STRING}}",
    "token": "{{STRING}}",
    "focusedItemToken": "{{STRING}}",
    "visibleTokenList": [
      "{{STRING}}"
    ]
  }
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| token | string | N | 클릭하는 template을 식별하기 위한 unique identifier |
| focusedItemToken | string | N | 현재 화면에 List Template이 보여지고 있을 때, 포커스된 item을 식별하기 위한 unique identifier focusable이 true인 List Template이 보여지고 있을 때는 반드시 focusedItemToken이 존재해야 함 |
| visibleTokenList | list | N | 현재 화면에 List Template이 보여지고 있을 때, 보여지고 있는 item들을 식별하기 위한 unique identifier 목록 List Template이 보여지고 있을 때는 반드시 visibleTokenList이 존재해야 함 |

## Common Objects

Template 에 사용되는 공통 object 의 데이터 구조입니다.

### ImageObject

```text
{
  "contentDescription": "{{STRING}}",
  "sources": [
    {
      "url": "{{STRING}}",
      "size": "{{STRING}}",
      "widthPixels": {{LONG}},
      "heightPixels": {{LONG}}
    }
  ]
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| contentDescription | string | N | - |
| sources | list | Y | 리스트로 제공되며 클라이언트에서 화면 크기에 가장 적합한 이미지를 사용해야 함 |
| sources.url | string | Y | - |
| sources.size | string | N | X\_SMALL, SMALL, MEDIUM, LARGE, X\_LARGE |
| sources.widthPixels | long | N | - |
| sources.heightPixels | long | N | - |

| size value | Recommended Size \(in pixels\) |
| :--- | :--- |
| X\_SMALL | 480 x 320 |
| SMALL | 720 x 480 |
| MEDIUM | 960 x 640 |
| LARGE | 1280 x 800 |
| X\_LARGE | 1920 x 1080 |

### TextObject

```text
{
  "text": "{{STRING}}",
  "color": "{{STRING}}",
  "style": {}
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| text | string | Y | Text 중간에 강조 표현을 위한 마크업 사용 가능 스펙 - 볼드 : &lt;b&gt;볼드&lt;/b&gt; - 기울림 : &lt;i&gt;기울림&lt;/i&gt; - 밑줄 : &lt;u&gt;밑줄&lt;/u&gt; - 윗첨자 : &lt;sup&gt;윗첨자&lt;/sup&gt; - 아래첨자 : &lt;sub&gt;아래첨자&lt;/sub&gt; - 취소선 : &lt;s&gt;취소선&lt;/s&gt; - 색상 : &lt;font color="red"&gt;빨강&lt;/font&gt;  위에 요소외 다른 마크업 사용 시 마크업 요소 사용 불가, 원본 표시 |
| color | string | N | color 형식 \(RGB\)  default 값은 디바이스마다 다름 |
| style | object | N | 기본적으로는 상위 스타일\(directive 등\)을 따름.  CSS 속성은 모두 가능하며, 다음의 값들을 가질 수 있다. - text-align : left, center, right - opacity : 0 ~ 1 - display : block, inline, none - margin : 10px - 사용예.  { "text-align":"center", "display": "block" } |

### ButtonObject

```text
{
  "type": "{{STRING}}",
  "text": "{{STRING}}",
  "image": ImageObject,
  "token": "{{STRING}}",
  "textInput": {
    "text": "{{STRING}}",
    "playServiceId": "{{STRING}}"
  },
  "postback": {},
  "autoTrigger": {
    "delayInMilliseconds": {{LONG}},
    "showTimer": {{BOOL}}
  },
  "closeTemplateAfter": {{BOOL}},
  "style": {},
  "disable": {{BOOL}}
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| type | string | N | text\(default\), image 중 하나의 값을 가질 수 있습니다. |
| image | [ImageObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#imageobject) | N | 버튼 이미지 - type이 image인 경우에 한해 필수이며, 해당 이미지를 이용해 버튼을 표현한다. |
| text | string | N | 버튼 텍스트  - type이 text인 경우에 한해 필수이며, 해당 텍스트를 이용해 버튼을 표현한다. |
| token | string | Y | 클릭 시 전달될 토큰 값 |
| eventType | string | N | 클릭 시 플랫폼으로 전달하는 Event Type \(Capability 명과 Event를 모두 명시해야 함\) - **Display.ElementSelected** :  default \(eventType 값이 없는 경우 기본값\) - **Text.TextInput** |
| textInput | object | N | eventType == TextTextInput인 경우 필수 |
| textInput.text | string | Y | 전달할 텍스트 |
| textInput.playServiceId | string | N | 특정 Play로 지정하여 라우팅하는 경우 사용 |
| postback | object | N | 클릭 시 전달되는 임의의 Object - 버튼 클릭 시 동작을 위해 필요한 정보를 임의의 JSON 포맷으로 추가 가능  - 기존에 token을 이 용도로 활용하는 경우가 많았는데, token은 identifier 역할을 하도록 하기 위해 추가 |
| autoTrigger | object | N | 특정 시간이 지난 뒤 ElementSelected Event를 자동으로 발생시키는 경우 포함 하위 parameter들은 autoTrigger가 포함되면 모두 mandatory parameter |
| autoTrigger.delayInMilliseconds | long | Y | TTS 종료 후 trigger 시킬때까지의 시간 \(msec\) |
| autoTrigger.showTimer | bool | Y | 버튼에 timer 숫자를 보여줄지 설정 |
| closeTemplateAfter | bool | N | trigger 또는 클릭 동작 후 template을 바로 닫을지, 아니면 template의 life cycle 대로 화면에 보여줄지 설정 |
| style | object | N | 버튼의 추가적인 style을 정의함. textObject의 style고 사용법이 동일함. |
| disable | bool | N | 이 속성이 true이면 버튼을 disable 처리함. |

### TitleObject

```text
{
  "logo": ImageObject,
  "text": TextObject,
  "subtext": TextObject,
  "subicon": ImageObject,
  "button": ButtonObject
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| logo | [ImageObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#imageobject) | N | png 타입으로 투명 이미지로 제공해야 함 |
| text | [TextObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#textobject) | Y | 제목 |
| subtext | [TextObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#textobject) | N | ASR Text 등 부제목 |
| subicon | [ImageObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#imageobject) | N | 서브 아이콘 \( 위치 : subText 왼쪽 \) |
| button | [ButtonObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#buttonobject) | N | 우측에 위치하는 버튼 |

### BackgroundObject

```text
{
  "image": ImageObject,
  "color": "{{STRING}}"
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| image | [ImageObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#imageobject) | N | - |
| color | string | N | color형식\(RGB\) default : \#000000 |

### Duration

TTS, 보이스 크롭 등이 종료된 후 template 이 화면에 남아 있어야 하는 시간입니다.

| Duration string | Duration value |
| :--- | :--- |
| SHORT | 7초 |
| MID | 15초 |
| LONG | 30초 |
| LONGEST | 10분 |

### GrammarGuide

발화가이드 입니다.

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| grammarGuide | array of string | N | 화면에 표시할 문자열들을 정의합니다. 사용예 : \["홈 화면으로 이동해줘", "선호채널 찾아줘"\] |

### StyleGrammarGuide

GrammarGuide의 확장된 발화가이드 입니다.

```text
[
    {
        "text": "{{STRING}}",
        "type": "{{STRING}}",
        "style": {}
    }
]
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| text | string | Y | 화면에 표시할 문자열들을 정의합니다. |
| type | string | Y | NONE, NUDGE, STYLE NONE: 기본 UI NUDGE: 넛지 UI STYLE: style 필드를 사용 |
| style | object | N | uiType 이 STYLE 일 때, 필수 CSS 속성은 모두 가능 |

### FloatingBannerObject

Banner에 사용되는 image object 입니다.

```text
{
    "image": ImageObject,
    "style": Object
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| image | [ImageObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#imageobject) | N | banner에 사용되는 image object |
| style | object | N | banner에 적용되는 style object. 사용예 : style: { right: "115px", bottom: "430px" } |

### ToggleButtonObject

```text
{
  "style": "{{STRING}}",
  "status": "{{STRING}}",
  "token": "{{STRING}}"
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| style | string | Y | image, text |
| status | string | Y | on, off |
| token | string | Y | 클릭 시 전달될 토큰 값 |

### ContextLayer

Template 의 종류를 구분하기 위한 속성입니다.

| contextLayer | description |
| :--- | :--- |
| INFO | 기본값. 정보성 |
| MEDIA | 미디어 재생 |
| ALERT | 알람/타이머 |
| CALL | 전화 수신/발신/통화중 |

### BadgeObject

```text
{
  "type": "{{STRING}}",
  "text": TextObject,
  "image": ImageObject
}
```

| parameter | type | mandatory | description |
| :--- | :--- | :--- | :--- |
| type | string | Y | - TEXT - IMAGE |
| text | [TextObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#textobject) | N | - |
| image | [ImageObject](../../../nugu-play/create-plays-with-play-builder/use-backend-proxy/capability-interfaces/display-interface.md#imageobject) | N | - |

