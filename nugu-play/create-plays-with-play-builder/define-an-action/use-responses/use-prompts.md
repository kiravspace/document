# Prompt 사용하기

## Prompt 사용하기 <a id="use-prompts"></a>

Prompt는 사용자에게 응답으로 전달할 메시지를 의미합니다. Prompt를 작성할때 다음과 같은 구성 요소들을 사용할 수 있습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xAD6C;&#xC131; &#xC694;&#xC18C;</th>
      <th style="text-align:left">&#xD558;&#xC704; &#xC694;&#xC18C;</th>
      <th style="text-align:left">&#xD2B9;&#xC9D5;</th>
      <th style="text-align:left">
        <p>&#xC790;&#xB3D9;&#xC644;&#xC131;</p>
        <p>&#xB2E8;&#xCD95;&#xD0A4;</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xC77C;&#xBC18; &#xD14D;&#xC2A4;&#xD2B8;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&apos;&#xAC00;&#xB098;&#xB2E4;&apos;&#xC640; &#xAC19;&#xC740; &#xC77C;&#xBC18;&#xC801;&#xC778;
        &#xD14D;&#xC2A4;&#xD2B8;&#xB97C; &#xADF8;&#xB300;&#xB85C; &#xC77D;&#xC5B4;
        &#xBC1C;&#xD654;&#xD569;&#xB2C8;&#xB2E4;.</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Parameter</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>&#xC640; &#xAC19;&#xC740; &#xD615;&#xD0DC;&#xB85C; &#xC0AC;&#xC6A9;&#xD558;&#xBA70;,
          Parameter&#xC5D0; &#xB2F4;&#xAE34; &#xAC12;&#xC744;</p>
        <p>&#xD14D;&#xC2A4;&#xD2B8;&#xB85C; &#xBCC0;&#xD615;&#xD558;&#xC5EC; &#xBC1C;&#xD654;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>Parameter &#xC0AC;&#xC6A9;&#xBC95;&#xC5D0; &#xB300;&#xD55C; &#xC790;&#xC138;&#xD55C;
          &#xB0B4;&#xC6A9;&#xC740;</p>
        <p><a href="../use-parameters/">Parameter &#xC0AC;&#xC6A9;&#xD558;&#xAE30;</a>&#xB97C;
          &#xCC38;&#xACE0;&#xD558;&#xC138;&#xC694;.</p>
      </td>
      <td style="text-align:left">{{</td>
    </tr>
    <tr>
      <td style="text-align:left">Response Filter</td>
      <td style="text-align:left">NLG Translator</td>
      <td style="text-align:left">
        <p>Parameter&#xC640; &#xD56D;&#xC0C1; &#xACB0;&#xD569;&#xD558;&#xC5EC; &#xC0AC;&#xC6A9;&#xB418;&#xBA70;,</p>
        <p>&#xB2E8;&#xB3C5;&#xC73C;&#xB85C; &#xC4F0;&#xC77C; &#xC218; &#xC5C6;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">&gt;</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">NLG Normalizer</td>
      <td style="text-align:left">
        <p>Parameter&#xC5D0; &#xB2F4;&#xACA8; &#xC788;&#xB294; &#xAC12;&#xC774; Filter&#xC758;
          Source&#xC640;</p>
        <p>100% &#xC77C;&#xCE58;&#xD560; &#xACBD;&#xC6B0;&#xC5D0;&#xB9CC; &#xB3D9;&#xC791;&#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">=</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">NLG Function</td>
      <td style="text-align:left">
        <p>Response Filter&#xC5D0; &#xB300;&#xD55C; &#xC790;&#xC138;&#xD55C; &#xB0B4;&#xC6A9;&#xC740;</p>
        <p><a href="../../define-response-filters.md">Response Filter</a>&#xB97C;
          &#xCC38;&#xACE0;&#xD558;&#xC138;&#xC694;.</p>
      </td>
      <td style="text-align:left">:</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC870;&#xC0AC;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>&apos;&#xC744;/&#xB97C;&apos;&#xACFC; &#xAC19;&#xC774; &#xC55E; &#xC74C;&#xC808;&#xC5D0;
          &#xB530;&#xB77C; &#xC870;&#xC0AC;&#xAC00; &#xBC14;&#xB00C;&#xB294; &#xACBD;&#xC6B0;&#xC5D0;</p>
        <p>&#xC790;&#xB3D9;&#xC73C;&#xB85C; &#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xBC1C;&#xD654;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC870;&#xC0AC; &#xC790;&#xB3D9; &#xBCC0;&#xD658;&#xC740; Parameter&#xC640;
          &#xD568;&#xAED8; &#xC0AC;&#xC6A9;&#xB420; &#xB54C;&#xB9CC; &#xB3D9;&#xC791;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC870;&#xC0AC; &#xCC98;&#xB9AC;&#xC5D0; &#xB300;&#xD55C; &#xC790;&#xC138;&#xD55C;
          &#xB0B4;&#xC6A9;&#xC740; <a href="use-prompts.md#process-postpositions">&#xC870;&#xC0AC; &#xCC98;&#xB9AC;&#xD558;&#xAE30;</a>&#xB97C;
          &#xCC38;&#xACE0;&#xD558;&#xC138;&#xC694;.</p>
      </td>
      <td style="text-align:left">/</td>
    </tr>
    <tr>
      <td style="text-align:left">SKML &#xD0DC;&#xADF8;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>TTS &#xC5D4;&#xC9C4;&#xC774; &#xD14D;&#xC2A4;&#xD2B8; &#xD639;&#xC740;
          Parameter&#xC758; &#xAC12;&#xC744;</p>
        <p>SKML &#xD0DC;&#xADF8;&#xC5D0; &#xB530;&#xB77C; &#xBC1C;&#xD654;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>SKML &#xD0DC;&#xADF8; &#xC0AC;&#xC6A9; &#xB300;&#xD55C; &#xC790;&#xC138;&#xD55C;
          &#xB0B4;&#xC6A9;&#xC740;</p>
        <p><a href="use-prompts.md#use-utterance-options">&#xBC1C;&#xD654; &#xC635;&#xC158; &#xC0AC;&#xC6A9;&#xD558;&#xAE30;</a>&#xB97C;
          &#xCC38;&#xACE0;&#xD558;&#xC138;&#xC694;.</p>
      </td>
      <td style="text-align:left">&lt;</td>
    </tr>
  </tbody>
</table>

#### Prompt의 유형 <a id="prompt-types"></a>

Play Builder의 Prompt에는 3가지 유형이 있습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xC720;&#xD615;</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xB300;&#xAE30; Prompt</td>
      <td style="text-align:left">Prompt&#xAC00; &#xBC1C;&#xD654;&#xB41C; &#xC774;&#xD6C4; Play&#xC758;
        &#xC138;&#xC158;&#xC774; &#xC720;&#xC9C0;&#xB429;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC5F0;&#xC18D; Prompt</td>
      <td style="text-align:left">
        <p>&#xB4A4;&#xC774;&#xC5B4; &#xC62C; Prompt&#xAC00; &#xC788;&#xB294; &#xACBD;&#xC6B0;&#xC5D0;&#xB9CC;
          &#xBC1C;&#xD654;&#xB418;&#xBA70;,</p>
        <p>&#xB4A4;&#xC774;&#xC5B4; &#xC624;&#xB294; Prompt&#xC640; &#xB354;&#xD574;&#xC838;&#xC11C;
          &#xD558;&#xB098;&#xC758; &#xBB38;&#xC7A5;&#xCC98;&#xB7FC; &#xBC1C;&#xD654;&#xB429;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC885;&#xB8CC; Prompt</td>
      <td style="text-align:left">Prompt&#xAC00; &#xBC1C;&#xD654;&#xB41C; &#xC774;&#xD6C4; Play&#xC758;
        &#xC138;&#xC158;&#xC774; &#xC885;&#xB8CC;&#xB429;&#xB2C8;&#xB2E4;.</td>
    </tr>
  </tbody>
</table>

Prompt는 사용 위치에 따라 다음과 같이 구분됩니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xC704;&#xCE58;</th>
      <th style="text-align:left"></th>
      <th style="text-align:left">&#xD2B9;&#xC9D5;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xC77C;&#xBC18; Response&#xC758; Prompt</td>
      <td style="text-align:left">Welcome Action&#xC744; &#xC81C;&#xC678;&#xD55C; &#xBAA8;&#xB4E0; Action</td>
      <td
      style="text-align:left">
        <p>&#xB300;&#xAE30; Prompt&#xC640; &#xC885;&#xB8CC; Prompt&#xAC00; &#xC0AC;&#xC6A9;&#xB429;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC5EC;&#xB7EC; Prompt&#xAC00; &#xC785;&#xB825;&#xB41C; &#xACBD;&#xC6B0;,
          &#xBB34;&#xC791;&#xC704;&#xB85C; &#xC120;&#xD0DD;&#xB418;&#xC5B4; &#xBC1C;&#xD654;&#xB429;&#xB2C8;&#xB2E4;.</p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Built-in Action &gt; welcome</td>
      <td style="text-align:left">
        <p>&#xB300;&#xAE30; Prompt&#xC640; &#xC5F0;&#xC18D; Prompt&#xAC00; &#xC0AC;&#xC6A9;&#xB429;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC5EC;&#xB7EC; Prompt&#xAC00; &#xC785;&#xB825;&#xB41C; &#xACBD;&#xC6B0;,
          &#xBB34;&#xC791;&#xC704;&#xB85C; &#xC120;&#xD0DD;&#xB418;&#xC5B4; &#xBC1C;&#xD654;&#xB429;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Built-in Action &gt; exit</td>
      <td style="text-align:left">
        <p>&#xC885;&#xB8CC; Prompt&#xAC00; &#xC0AC;&#xC6A9;&#xB429;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC5EC;&#xB7EC; Prompt&#xAC00; &#xC785;&#xB825;&#xB41C; &#xACBD;&#xC6B0;,
          &#xBB34;&#xC791;&#xC704;&#xB85C; &#xC120;&#xD0DD;&#xB418;&#xC5B4; &#xBC1C;&#xD654;&#xB429;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Built-in Action &gt; fallback</td>
      <td style="text-align:left">
        <p>&#xB300;&#xAE30; Prompt&#xC640; &#xC885;&#xB8CC; Prompt&#xAC00; &#xC0AC;&#xC6A9;&#xB429;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC5EC;&#xB7EC; Prompt&#xAC00; &#xC785;&#xB825;&#xB41C; &#xACBD;&#xC6B0;,
          &#xC704;&#xC5D0;&#xC11C;&#xBD80;&#xD130; &#xC21C;&#xCC28;&#xC801;&#xC73C;&#xB85C;
          &#xBC1C;&#xD654;&#xB429;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Slot-filling Prompt</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>&#xB300;&#xAE30; Prompt&#xC640; &#xC885;&#xB8CC; Prompt&#xAC00; &#xC0AC;&#xC6A9;&#xB429;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC5EC;&#xB7EC; Prompt&#xAC00; &#xC785;&#xB825;&#xB41C; &#xACBD;&#xC6B0;,
          &#xC704;&#xC5D0;&#xC11C;&#xBD80;&#xD130; &#xC21C;&#xCC28;&#xC801;&#xC73C;&#xB85C;
          &#xBC1C;&#xD654;&#xB429;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC608;&#xC678; &#xC0C1;&#xD669; &#xCC98;&#xB9AC;&#xC758; Exception Prompt</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">
          <p>&#xB300;&#xAE30; Prompt&#xC640; &#xC885;&#xB8CC; Prompt&#xAC00; &#xC0AC;&#xC6A9;&#xB429;&#xB2C8;&#xB2E4;.</p>
          <p>&#xC5EC;&#xB7EC; Prompt&#xAC00; &#xC785;&#xB825;&#xB41C; &#xACBD;&#xC6B0;,
            &#xC704;&#xC5D0;&#xC11C;&#xBD80;&#xD130; &#xC21C;&#xCC28;&#xC801;&#xC73C;&#xB85C;
            &#xBC1C;&#xD654;&#xB429;&#xB2C8;&#xB2E4;.</p>
        </td>
    </tr>
  </tbody>
</table>

#### Silent Prompt <a id="silent-prompt"></a>

사용자에게 빈 응답을 전달하고 싶을 경우, Silent Prompt를 사용할 수 있습니다. Silent Prompt는 Prompt 입력 창 우측의 버튼을 눌러 설정 가능합니다. Silent Prompt를 응답으로 설정하면, 아무 발화 없이 대기 모드로 넘어가거나 세션이 종료되므로 꼭 필요한 경우에만 사용하는 것이 좋습니다. Silent Prompt는 모든 유형의 Prompt에서 사용할 수 있습니다.

![](../../../../.gitbook/assets/silentprompt.gif)

## 조사 처리하기 <a id="process-postpositions"></a>

국어의 조사 '이/가, 을/를, 은/는, 과/와, 로/으로'는 같은 형태소지만 앞음절의 받침 유무에 따라 다르게 사용됩니다.

Prompt를 입력할 때 일반 문장은 작성자가 입력한 조사를 그대로 사용하면 되나, Parameter를 사용하는 경우에는 그 Parameter에 담긴 마지막 글자의 받침 유무를 알 수 없기 때문에 별도의 처리를 하지 않는다면 '내일는'과 같이 조사가 잘못 붙어서 응답될 가능성이 있습니다. Play Builder에서는 Parameter 뒤에 조사를 쓰는 경우 Parameter에 담긴 마지막 글자의 받침 유무에 따라 자동으로 조사를 변환 처리합니다.

Parameter의 `}}` 기호 뒤에 / 입력하면 조사의 자동완성 창이 표시됩니다. 이 창에서 원하는 조사를 선택합니다.

![](../../../../.gitbook/assets/ch3_323411_01-1.png)

다음과 같이 중괄호 사이에 대표 조사가 입력되지만, 실제 발화 시에는 Parameter 마지막 글자의 받침 여부 따라 조사가 변환되어 출력됩니다.

![](../../../../.gitbook/assets/ch3_323411_02-1.png)

자동완성을 사용하지 않더라도 parameter의 `}}` 사이에 조사를 직접 입력해도 정상 동작합니다.

받침 유무에 따른 조사는 다음과 같이 변환됩니다.

|  | 은/는 | 이/가 | 을/를 | 과/와 | 로/으로 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 받침이 없는 경우 | 는 | 가 | 를 | 와 | 로 |
| 받침이 있는 경우 | 은 | 이 | 을 | 과 | 으로 |

#### 조사 처리 시, 받침 유무 판정 규칙

* 알파벳은 미국식 영어로 읽는 것을 한국어로 옮긴다고 간주하고 조사 처리합니다. 
* 10 g, 1 m와 같이 숫자와 단위가 붙어서 조합되고, [발화 옵션 Say 태그\(단위 속성\)](../../../../reference/list-of-unit-tags-supported-by-utterance-options.md)를 처리하지 않은 경우, 10 그램, 1 미터와 같이 단위에 대한 표준어로 변환하여 조사를 붙입니다. 
* 괄호나 특수문자가 포함된다면 제거한 후 처리합니다. 
* 단위, 한글, 영문, 숫자에 해당하지 않는 경우는 변환하지 않습니다.

## 발화 옵션 사용하기 <a id="use-utterance-options"></a>

입력한 Response의 Prompt를 TTS 엔진이 음성으로 변환할 때 예상과는 다른 방식으로 읽을 수도 있고, 때로는 천천히 읽거나 또박또박 읽게 하고 싶을 수도 있습니다.

가령 '119로 전화를 걸겠습니다'라고 Prompt를 입력한 경우 '일일구로 전화를 걸겠습니다'라고 발화할 것이라 기대하지만, TTS 엔진은 기본적으로 숫자를 그대로 읽도록 처리하고 있기 때문에 '백십구로 전화를 걸겠습니다.' 라고 읽게 됩니다.

Play Builder는 입력한 Prompt를 음성으로 변환시킬 때 개별적으로 튜닝을 하거나, 다르게 읽을 수 있는 '발화 옵션' 기능을 제공하고 있습니다. 발화 옵션은 Play의 모든 Prompt에 일괄 반영할 수도 있고, 특정 문장별로 변경할 수 있습니다.

또, 문장 내 발화 옵션 태그를 사용하여 세밀한 설정도 가능합니다.

#### 전체 발화 옵션 변경하기

1\) Play 내 모든 prompt의 발화 옵션을 변경하고 싶다면 `General` &gt; `기본정보` 로 이동 합니다.

![](../../../../.gitbook/assets/ch3_323413_c01.png)

2\) 기본 정보 페이지의 Prompt 발화 옵션에서 발화속도, 음 높낮이, 문장 사이의 묵음 길이, 끊어읽기 뒤 묵음 길이를 설정한 후 `발화옵션 적용하기` 버튼을 클릭합니다. 이 값을 변경하면 변경한 순간 이후부터 만드는 Prompt부터 적용됩니다.

![](../../../../.gitbook/assets/ch3_323413_c02.png)

**① 발화속도 \(speed\)** 재생 속도를 50 ~ 120% 사이에서 변경할 수 있습니다.\(기본값: 100%\) 최솟값이나 최댓값으로 설정할 경우에는 음질 열화가 발생할 수 있으므로 85 ~ 115 사잇값 사용을 권장합니다.

**② 합성음 높낮이 \(pitch\)** 합성음의 높낮이를 90 ~ 110 % 사이에서 변경할 수 있습니다.\(기본값: 100%\) 최솟값이나 최댓값으로 설정할 경우에는 음질 열화가 발생할 수 있으므로 95 ~ 105 사잇값 사용을 권장합니다.

**③ 문장 사이 묵음 길이 \(pause1\)** 문장과 문장 사이의 묵음 길이를 300 ~ 900 ms 사이에서 변경할 수 있습니다.\(기본값: 600 ms\)

**④ 끊어읽기 뒤 묵음 길이 \(pause2\)** 문장 내 끊어읽기 후의 묵음 길이를 100 ~ 500 ms 사이에서 변경할 수 있습니다.\(기본값: 300 ms\)

### 문장별 발화 옵션 변경하기

문장별로 발화 옵션을 조절할 수 있습니다.

1\) Play Builder 홈 화면에서 모든 Prompt의 발화 옵션을 변경할 Play를 클릭하여 선택한 후 `Actions` &gt; `Custom Actions` 페이지에서 발화 옵션을 설정할 문장이 있는 Action을 선택합니다.

![](../../../../.gitbook/assets/ch3_323413_c03.png)

2\) Output 정의 영역에서 발화 옵션을 변경할 Prompt의 우측 버튼을 클릭하여 옵션을 설정한 후 \[Play 저장\] 버튼을 클릭합니다.

* 변경 가능한 옵션은 전체 발화 옵션과 같습니다.

![](../../../../.gitbook/assets/ch3_323413_c04.png)

### 문장 내 발화 옵션 태그 추가하기 <a id="skml-tag"></a>

Prompt 내에서 특정 구간에 끊어읽기를 추가하거나, 특정 단어를 읽는 방식을 조절하는 태그도 제공하고 있습니다.

태그들은 기본적으로 `<태그 속성="속성값">` 형태로 구성됩니다. 이 태그는 직접 입력하지 않아도 되도록 Prompt 문장 입력창에서 자동완성으로 제공하고 있습니다. 문장 입력 중 특수문자 `<`를 입력한 뒤 자동완성창에서 세 가지 기능 중 적용할 옵션을 선택합니다.

![](../../../../.gitbook/assets/ch3_323413_01-1.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xBC1C;&#xD654; &#xC635;&#xC158;</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>&#xD14D;&#xC2A4;&#xD2B8;&#xC77D;&#xAE30;</p>
        <p>(say)</p>
      </td>
      <td style="text-align:left">
        <p>&#xD55C;&#xAE00;&#xC774; &#xC544;&#xB2CC; &#xBB38;&#xC790;&#xB4E4;&#xC744;
          &#xC5B4;&#xB5BB;&#xAC8C; &#xC77D;&#xC744;&#xC9C0; &#xACB0;&#xC815;&#xD558;&#xB294;
          &#xD0DC;&#xADF8;&#xC785;&#xB2C8;&#xB2E4;.</p>
        <p>&apos;4-2&apos;&#xB294; &apos;&#xC0AC; &#xB2E4;&#xC2DC; &#xC774;&apos;&#xC640;
          &#xAC19;&#xC774; &#xC8FC;&#xC18C;&#xCC98;&#xB7FC; &#xC77D;&#xAC70;&#xB098;,</p>
        <p>&apos;&#xC0AC; &#xB300; &#xC774;&apos;&#xCC98;&#xB7FC; &#xACBD;&#xAE30;
          &#xC2A4;&#xCF54;&#xC5B4;&#xB85C; &#xC77D;&#xC744; &#xC218; &#xC788;&#xC744;
          &#xC218; &#xC788;&#xAE30; &#xB54C;&#xBB38;&#xC5D0;,</p>
        <p>&#xC774;&#xAC83;&#xC744; &#xC5B4;&#xB5BB;&#xAC8C; &#xC77D;&#xC744; &#xAC83;&#xC778;&#xC9C0;
          &#xD0DC;&#xADF8;&#xB85C; &#xC815;&#xD574;&#xC8FC;&#xB294; &#xAE30;&#xB2A5;&#xC785;&#xB2C8;&#xB2E4;.</p>
        <p>&#xD0DC;&#xADF8;&#xB97C; &#xC801;&#xC6A9;&#xD560; &#xD14D;&#xC2A4;&#xD2B8;&#xC758;
          &#xB05D;&#xC5D0; <code>&lt;/say&gt;</code>&#xAC00; &#xD544;&#xC218;&#xB85C;
          &#xB4E4;&#xC5B4;&#xAC00;&#xC57C; &#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xC77D;&#xAE30; (sub)</td>
      <td style="text-align:left">
        <p>&#xC77C;&#xBC18;&#xC801;&#xC774;&#xC9C0; &#xC54A;&#xC740; &#xBC1C;&#xC74C;&#xBCC0;&#xD658;
          &#xADDC;&#xCE59;&#xC744; &#xD1B5;&#xD574; &#xBC1C;&#xC74C;&#xC774; &#xB418;&#xB294;
          &#xD14D;&#xC2A4;&#xD2B8;&#xC778; &#xACBD;&#xC6B0;,</p>
        <p>&#xC18D;&#xC131;&#xC73C;&#xB85C; &#xC9C0;&#xC815;&#xD574;&#xC900; &#xD14D;&#xC2A4;&#xD2B8;&#xB85C;
          &#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xBC1C;&#xD654;&#xD558;&#xB3C4;&#xB85D;
          &#xD558;&#xB294; &#xD0DC;&#xADF8;&#xC785;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) <code>&lt;sub alias=&quot;&#xD638;&#xB0A0;&#xB450;&quot;&gt;Ronaldo&lt;/sub&gt;</code> &#x2192;
          &apos;Ronaldo&apos;&#xB97C;</p>
        <p>&#xD0DC;&#xADF8; &#xB0B4; &#xC18D;&#xC131;&#xC758; &apos;&#xD638;&#xB0A0;&#xB450;&apos;&#xB85C;
          &#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) <code>&lt;sub alias=&quot;&#xC368;&#xD504;&#xB77C;&#xC774;&#xC988;&quot;&gt;&#xC11C;&#xD504;&#xB77C;&#xC774;&#xC988;&lt;/sub&gt;</code> &#x2192;
          &apos;&#xC11C;&#xD504;&#xB77C;&#xC774;&#xC988;&apos;&#xB97C;</p>
        <p>&#xD0DC;&#xADF8; &#xB0B4; &#xC18D;&#xC131;&#xC758; &apos;&#xC368;&#xD504;&#xB77C;&#xC774;&#xC988;&apos;&#xB85C;
          &#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xD0DC;&#xADF8;&#xB97C; &#xC801;&#xC6A9;&#xD560; &#xD14D;&#xC2A4;&#xD2B8;&#xC758;
          &#xB05D;&#xC5D0; <code>&lt;/sub&gt;</code>&#xAC00; &#xD544;&#xC218;&#xB85C;
          &#xB4E4;&#xC5B4;&#xAC00;&#xC57C; &#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>&#xB04A;&#xC5B4;&#xC77D;&#xAE30;</p>
        <p>(break, pause)</p>
      </td>
      <td style="text-align:left">
        <p>&#xBB38;&#xC7A5;&#xC744; &#xC77D;&#xC744; &#xB54C; &#xB0B4;&#xC6A9;&#xC0C1;,
          &#xAE38;&#xC774;&#xC0C1; &#xC801;&#xC808;&#xD558;&#xAC8C; &#xC26C;&#xC5B4;&#xC11C;
          &#xC77D;&#xC5B4;&#xC8FC;&#xB294; &#xACF3;&#xC744; &#xACB0;&#xC815;&#xD558;&#xB294;
          &#xD0DC;&#xADF8;&#xC785;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC785;&#xB825;&#xB41C; Prompt&#xB294; TTS &#xC5D4;&#xC9C4;&#xC774; &#xB04A;&#xC5B4;&#xC77D;&#xAE30;
          &#xAC04;&#xACA9;&#xC744; &#xC2A4;&#xC2A4;&#xB85C; &#xACC4;&#xC0B0;&#xD558;&#xC5EC;
          &#xBC1C;&#xD654;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>TTS &#xC5D4;&#xC9C4; &#xD569;&#xC131;&#xC74C;&#xC758; &#xB04A;&#xC5B4;&#xC77D;&#xAE30;&#xAC00;
          &#xC790;&#xC5F0;&#xC2A4;&#xB7FD;&#xC9C0; &#xC54A;&#xB2E4;&#xACE0; &#xD310;&#xB2E8;&#xB420;
          &#xACBD;&#xC6B0;&#xC5D0;</p>
        <p>&#xB04A;&#xC5B4;&#xC77D;&#xAE30;&#xC758; &#xC704;&#xCE58; &#xBC0F; &#xC885;&#xB958;&#xB97C;
          &#xC218;&#xB3D9;&#xC73C;&#xB85C; &#xC124;&#xC815;&#xD560; &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC774; &#xD0DC;&#xADF8;&#xB294; &#xC801;&#xC6A9;&#xD560; &#xC5B4;&#xC808;&#xC758;
          &#xB4A4;&#xC5D0; &#xACF5;&#xBC31; &#xC5C6;&#xC774; &#xB123;&#xC5B4;&#xC57C;&#xD558;&#xACE0;,
          &#xD0DC;&#xADF8;&#xC758; &#xB4A4;&#xC5D0;&#xB294; &#xACF5;&#xBC31;&#xC774;
          &#xC788;&#xC5B4;&#xC57C; &#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) <code>&#xC548;&#xB155;&#xD558;&#xC138;&#xC694;. &lt;break type=&quot;weak&quot;/&gt;&#xC544;&#xB9AC;&#xC544;&#xC5D0;&#xC694;.</code>(X)</p>
        <p>&#xC608;) <code>&#xC548;&#xB155;&#xD558;&#xC138;&#xC694;.&lt;break type=&quot;weak&quot;/&gt; &#xC544;&#xB9AC;&#xC544;&#xC5D0;&#xC694;.</code>(O)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&#xD6A8;&#xACFC;&#xC74C;&#xB123;&#xAE30; (audio)</td>
      <td style="text-align:left">&#xBB38;&#xC7A5; &#xC911;&#xAC04;&#xC5D0; &#xBC15;&#xC218; &#xC18C;&#xB9AC;,
        &#xCC9C;&#xB465; &#xC18C;&#xB9AC; &#xB4F1;&#xC758; &#xD6A8;&#xACFC;&#xC74C;&#xC744;
        &#xB123;&#xC744; &#xC218; &#xC788;&#xB294; &#xD0DC;&#xADF8;&#xC785;&#xB2C8;&#xB2E4;.</td>
    </tr>
  </tbody>
</table>

각 태그별 세부 기능은 다음과 같습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>&#xC0C1;&#xC704;</p>
        <p>&#xC635;&#xC158;</p>
      </th>
      <th style="text-align:left">&#xC138;&#xBD80; &#xC635;&#xC158;</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
      <th style="text-align:left">&#xC18D;&#xC131;</th>
      <th style="text-align:left">&#xC785;&#xB825;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>&#xB04A;&#xC5B4;</p>
        <p>&#xC77D;&#xAE30;</p>
      </td>
      <td style="text-align:left">&#xAC00;&#xC7A5; &#xAE38;&#xAC8C; &#xB04A;&#xC5B4;&#xC77D;&#xAE30;</td>
      <td
      style="text-align:left">
        <p>&#xAC00;&#xC7A5; &#xAE38;&#xAC8C; &#xB04A;&#xC5B4;&#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) &#xC624;&#xB298;&#xC740; &#xBE44;&#xAC00;&lt;break type=&quot;sentence&quot;/&gt;
          &#xC635;&#xB2C8;&#xB2E4;.</p>
        </td>
        <td style="text-align:left">sentence</td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xAE38;&#xAC8C; &#xB04A;&#xC5B4;&#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&#xAE38;&#xAC8C; &#xB04A;&#xC5B4;&#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) &#xC624;&#xB298;&#xC740; &#xBE44;&#xAC00;&lt;break type=&quot;strong&quot;/&gt;
          &#xC635;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">strong</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC9E7;&#xAC8C; &#xB04A;&#xC5B4;&#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&#xC9E7;&#xAC8C; &#xB04A;&#xC5B4;&#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) &#xC624;&#xB298;&#xC740; &#xBE44;&#xAC00;&lt;break type=&quot;weak&quot;/&gt;
          &#xC635;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">weak</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xB04A;&#xC5B4;&#xC77D;&#xAE30; &#xC5C6;&#xC560;&#xAE30;</td>
      <td style="text-align:left">
        <p>&#xC774; &#xD0DC;&#xADF8;&#xAC00; &#xCD94;&#xAC00;&#xB41C; &#xBD80;&#xBD84;&#xC744;</p>
        <p>&#xB04A;&#xC9C0; &#xC54A;&#xACE0; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC6D0;&#xD558;&#xC9C0; &#xC54A;&#xAC8C; &#xB04A;&#xC5B4;&#xC77D;&#xB294;
          &#xBD80;&#xBD84;&#xC774;</p>
        <p>&#xBC1C;&#xC0DD;&#xD558;&#xB294; &#xACBD;&#xC6B0;&#xC5D0; &#xC0AC;&#xC6A9;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) &#xBE0C;&#xB85C;&#xCF5C;&#xB9AC;&lt;break type=&quot;none&quot;/&gt;</p>
        <p>&#xB108;&#xB9C8;&#xC800;&#xC758; &#xC74C;&#xC545;&#xC744; &#xB4E4;&#xB824;&#xB4DC;&#xB9B4;&#xAED8;&#xC694;.</p>
      </td>
      <td style="text-align:left">none</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD55C;&#xB2E8;&#xC5B4;&#xCC98;&#xB7FC; &#xBD99;&#xC5EC;&#xC77D;&#xAE30;</td>
      <td
      style="text-align:left">
        <p>&#xD55C; &#xB2E8;&#xC5B4;&#xC640; &#xAC19;&#xC774; &#xBC1C;&#xC74C;&#xB418;&#xB3C4;&#xB85D;
          &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;&#xB97C;&#xB4E4;&#xC5B4; &apos;&#xCCAB; &#xBC88;&#xC9F8;&apos;&#xB97C;
          &apos;&#xCCAB;&#xBED4;&#xC9F8;&apos;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) &#xCCAB;&lt;break type=&quot;clitic&quot;/&gt; &#xBC88;&#xC9F8;</p>
        </td>
        <td style="text-align:left">clitic</td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xB04A;&#xC5B4;&#xC77D;&#xAE30; &#xC2DC;&#xAC04;&#xC124;&#xC815;</td>
      <td
      style="text-align:left">
        <p>&#xB04A;&#xC5B4; &#xC77D;&#xB294; &#xC2DC;&#xAC04;&#xC744; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&lt;pause time=&quot;200&quot;/&gt;</p>
        <p>&#x2192; 200 ms &#xB3D9;&#xC548; &#xB04A;&#xC5B4; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&apos;0&apos;&#xBCF4;&#xB2E4; &#xD070; &#xC815;&#xC218;&#xB9CC; &#xC0AC;&#xC6A9;
          &#xAC00;&#xB2A5;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC608;) &#xC624;&#xB298;&#xC740;&lt;pause time=&quot;200&quot;/&gt;
          &#xBE44;&#xAC00; &#xC635;&#xB2C8;&#xB2E4;.</p>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">[n]</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xD14D;&#xC2A4;&#xD2B8;&#xC77D;&#xAE30;</td>
      <td style="text-align:left">&#xD55C;&#xC790; &#xB0B1;&#xC22B;&#xC790; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&#xC22B;&#xC790;&#xB97C; &apos;&#xC77C;, &#xC774;, &#xC0BC;, &#xC0AC;&apos;&#xC640;
          &#xAC19;&#xC774; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xB450; &#xC790;&#xB9AC; &#xC774;&#xC0C1;&#xC758; &#xC22B;&#xC790;&#xB3C4;
          &apos;&#xC77C;&#xC77C;&#xAD6C;&apos;&#xC640; &#xAC19;&#xC774;</p>
        <p>&#xD55C; &#xC790;&#xC529; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">digit</td>
      <td style="text-align:left">[n]</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD55C;&#xC790; &#xC22B;&#xC790; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&#xC22B;&#xC790;&#xB97C; &apos;&#xC77C;, &#xC774;, &#xC0BC;, &#xC0AC;&apos;&#xC640;
          &#xAC19;&#xC774; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC790;&#xB9BF;&#xC218;&#xB97C; &#xD3EC;&#xD568;&#xD558;&#xC5EC; &apos;&#xBC31;&#xC2ED;&#xAD6C;&apos;&#xC640;
          &#xAC19;&#xC774; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&apos;&#xACBD;&apos;(10&#xC758; 16&#xC81C;&#xACF1;) &#xB2E8;&#xC704;&#xAE4C;&#xC9C0;
          &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">num_hanja</td>
      <td style="text-align:left">[n]</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD55C;&#xAE00; &#xC22B;&#xC790; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">&#xC22B;&#xC790;&#xB97C; &apos;&#xD55C;, &#xB450;, &#xC138;, &#xB124;&apos;&#xC640;
        &#xAC19;&#xC774; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</td>
      <td style="text-align:left">num_kor</td>
      <td style="text-align:left">[n]</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC601;&#xC5B4; &#xC22B;&#xC790; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&#xC22B;&#xC790;&#xB97C; &apos;&#xC6D0;, &#xD22C;, &#xC4F0;&#xB9AC;, &#xD3EC;&apos;&#xC640;
          &#xAC19;&#xC774; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>Trillion(10&#xC758; 12&#xC81C;&#xACF1;) &#xB2E8;&#xC704;&#xAE4C;&#xC9C0;
          &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">num_eng</td>
      <td style="text-align:left">[n]</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xB0A0;&#xC9DC; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&apos;&#xC774;&#xCC9C;&#xC2ED;&#xD314;&#xB144; &#xC0BC;&#xC6D4; &#xAD6C;&#xC77C;&apos;&#xACFC;
          &#xAC19;&#xC774;</p>
        <p>&#xB0A0;&#xC9DC;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&apos;&#xC0BC;&#xC6D4; &#xAD6C;&#xC77C;&apos;&#xACFC; &#xAC19;&#xC774;
          &#xD2B9;&#xC815; &#xB0A0;&#xC9DC;&#xB85C; &#xC77D;&#xAC70;&#xB098;,</p>
        <p>&apos;&#xC0BC;&#xC6D4; &#xAD6C;&#xC77C;&#xC5D0;&#xC11C; &#xC0AC;&#xC6D4;
          &#xC2ED;&#xC77C;&apos;&#xACFC; &#xAC19;&#xC774;</p>
        <p>&#xBC94;&#xC704;&#xB85C; &#xC77D;&#xB294; &#xAC83;&#xC744; &#xC9C0;&#xC6D0;&#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">date</td>
      <td style="text-align:left">
        <p>&#xD2B9;&#xC815; &#xB0A0;</p>
        <p>[yyyy]-[mm]-[dd]</p>
        <p>[yyyy]:[mm]:[dd]</p>
        <p>[yyyy]/[mm]/[dd]</p>
        <p>[yyyy].[mm].[dd]</p>
        <p>[mm]-[dd]</p>
        <p>[mm]/[dd]</p>
        <p>[mm].[dd]</p>
        <p>&#xBC94;&#xC704;</p>
        <p>[yyyy]-[mm]-[dd]~</p>
        <p>[yyyy]-[mm]-[dd]</p>
        <p>[yyyy]:[mm]:[dd]~</p>
        <p>[yyyy]:[mm]:[dd]</p>
        <p>[yyyy]/[mm]/[dd]~[yyyy]/[mm]/[dd]</p>
        <p>[yyyy].[mm].[dd]~</p>
        <p>[yyyy].[mm].[dd]</p>
        <p>[mm]-[dd]~</p>
        <p>[mm]-[dd]</p>
        <p>[mm]/[dd]~</p>
        <p>[mm]/[dd]</p>
        <p>[mm].[dd]~</p>
        <p>[mm].[dd]</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC2DC;&#xAC04; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&apos;&#xC5F4;&#xD55C;&#xC2DC; &#xC0BD;&#xC2ED;&#xBD84; &#xC0AC;&#xC2ED;&#xC624;&#xCD08;&apos;&#xC640;
          &#xAC19;&#xC774;</p>
        <p>&#xC2DC;&#xAC04;&#xC73C;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&apos;hh&#xC2DC; mm&#xBD84; ss&#xCD08;, hh&#xC2DC; mm&#xBD84;&apos;&#xACFC;
          &#xAC19;&#xC774;</p>
        <p>&#xD2B9;&#xC815; &#xC2DC;&#xAC04;&#xC73C;&#xB85C; &#xC77D;&#xAC70;&#xB098;</p>
        <p>&apos;hh&#xC2DC; mm&#xBD84; ss&#xCD08;&#xC5D0;&#xC11C;</p>
        <p>hh&#xC2DC; mm&#xBD84; ss&#xCD08;&apos;,</p>
        <p>&apos;hh&#xC2DC; mm&#xBD84;&#xC5D0;&#xC11C; hh&#xC2DC; mm&#xBD84;&apos;&#xCC98;&#xB7FC;</p>
        <p>&#xBC94;&#xC704;&#xB85C; &#xC77D;&#xB294; &#xAC83;&#xC744; &#xC9C0;&#xC6D0;&#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">time</td>
      <td style="text-align:left">
        <p>&#xD2B9;&#xC815; &#xC2DC;&#xAC04;</p>
        <p>[hh]:[mm]:[ss]</p>
        <p>[mm]:[ss]</p>
        <p>&#xAE30;&#xAC04;</p>
        <p>[hh]:[mm]:[ss]~</p>
        <p>[hh]:[mm]:[ss]</p>
        <p>[hh]:[mm]:[ss]-</p>
        <p>[hh]:[mm]:[ss]</p>
        <p>[mm]:[ss]~</p>
        <p>[mm]:[ss]</p>
        <p>[mm]:[ss]-</p>
        <p>[mm]:[ss]</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xB2E8;&#xC704; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&apos;&#xCE60;&#xBBF8;&#xD130;, &#xCE60;&#xADF8;&#xB7A8;&apos;&#xACFC;
          &#xAC19;&#xC774; &#xB2E8;&#xC704;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>139&#xAC1C;&#xC758; &#xB2E8;&#xC704;&#xB97C; &#xC77D;&#xAE30; &#xC9C0;&#xC6D0;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>(<a href="use-prompts.md#list-of-unit-tags-supported-by-utterance-options">&#xBC1C;&#xD654; &#xC635;&#xC158;&#xC5D0;&#xC11C; UNIT</a>
        </p>
        <p><a href="use-prompts.md#list-of-unit-tags-supported-by-utterance-options">&#xD0DC;&#xADF8;&#xB85C; &#xC9C0;&#xC6D0; &#xB2E8;&#xC704; &#xBAA9;&#xB85D;</a>)</p>
      </td>
      <td style="text-align:left">unit</td>
      <td style="text-align:left">[n][unit]</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC8FC;&#xC18C; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&apos;&#xD314;&#xC2ED;&#xC0BC; &#xB2E4;&#xC2DC; &#xC77C;&apos;&#xACFC;
          &#xAC19;&#xC774; &#xC9C0;&#xBC88; &#xC8FC;&#xC18C;&#xC758;</p>
        <p>&#xC9C0;&#xBC88;&#xC744; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">address</td>
      <td style="text-align:left">[n]-[n]</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC804;&#xD654;&#xBC88;&#xD638; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&apos;&#xC77C;&#xC774;&#xC0BC;&#xC0AC; &#xC77C;&#xC774;&#xC0BC;&#xC0AC;&apos;&#xC640;
          &#xAC19;&#xC774;</p>
        <p>&#xC804;&#xD654;&#xBC88;&#xD638;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">telephone</td>
      <td style="text-align:left">
        <p>[n]-[n]</p>
        <p>[n]-[n]-[n]</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC601;&#xC5B4; &#xC2A4;&#xD3A0;&#xB9C1; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">
        <p>&apos;&#xBE44;&#xD2F0;&#xC5D0;&#xC2A4;&apos;&#xC640; &#xAC19;&#xC774;
          &#xC601;&#xC5B4; &#xC2A4;&#xD3A0;&#xB9C1;&#xC73C;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xB300;&#xC18C;&#xBB38;&#xC790;&#xB294; &#xAD6C;&#xBD84;&#xD558;&#xC9C0;
          &#xC54A;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
      <td style="text-align:left">spell</td>
      <td style="text-align:left">[text]</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xACBD;&#xAE30; &#xC2A4;&#xCF54;&#xC5B4; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">&apos;&#xC0BC; &#xB300; &#xC774;&apos;&#xC640; &#xAC19;&#xC774; &#xACBD;&#xAE30;
        &#xC2A4;&#xCF54;&#xC5B4;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</td>
      <td
      style="text-align:left">score</td>
        <td style="text-align:left">
          <p>[n]:[n]</p>
          <p>[n]-[n]</p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBD84;&#xC218; &#xC77D;&#xAE30;</td>
      <td style="text-align:left">&apos;&#xC0BC;&#xBD84;&#xC758; &#xC77C;&apos;&#xACFC; &#xAC19;&#xC774;
        &#xBD84;&#xC218;&#xB85C; &#xC77D;&#xC2B5;&#xB2C8;&#xB2E4;.</td>
      <td style="text-align:left">fraction</td>
      <td style="text-align:left">[n]/[n]</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xD6A8;&#xACFC;&#xC74C;&#xB123;&#xAE30;</td>
      <td style="text-align:left">&#xC2EC;&#xC7A5; &#xBC15;&#xB3D9;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC2EC;&#xC7A5; &#xBC15;&#xB3D9; (&#xBE60;&#xB974;&#xAC8C;)</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC7AC;&#xCC44;&#xAE30;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBC15;&#xC218;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD154;&#xB808;&#xD30C;&#xC2DC; 1</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD154;&#xB808;&#xD30C;&#xC2DC; 2</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBC1C;&#xAC78;&#xC74C;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBB3C;&#xD280;&#xAE30;&#xB294;&#xC18C;&#xB9AC;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC5BC;&#xAD74; &#xC53B;&#xB294; &#xC18C;&#xB9AC;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC74C;&#xC545; 1</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC74C;&#xC545; 2</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xCE74;&#xBA54;&#xB77C; &#xC154;&#xD130;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD540;&#xBC84;&#xD2BC; &#xB204;&#xB974;&#xB294; &#xC18C;&#xB9AC;</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBD88;&#xD0C0;&#xB294; &#xC18C;&#xB9AC;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xCC9C;&#xB465;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC790;&#xB3D9;&#xCC28; &#xB9AC;&#xBAA8;&#xCF58;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBE44;&#xD589;&#xAE30;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBB3C;&#xBC29;&#xC6B8; &#xB5A8;&#xC5B4;&#xC9C0;&#xB294; &#xC18C;&#xB9AC;</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD718;&#xD30C;&#xB78C; 1</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xD718;&#xD30C;&#xB78C; 2</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xBE57;&#xC790;&#xB8E8;&#xC9C8;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC885;&#xC18C;&#xB9AC; 1</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#xC885;&#xC18C;&#xB9AC; 2</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
Prompt 내에 사용하는 태그는 텍스트를 직접 입력하여 추가 또는 수정할 수 있습니다.
{% endhint %}

### 발화 옵션에서 UNIT 태그로 지원하는 단위 목록 <a id="list-of-unit-tags-supported-by-utterance-options"></a>

문장 내 발화 옵션 태그 중 `텍스트 읽기` &gt; `단위 읽기` 태그에서 지원하는 목록은 [단위 목록](../../../../reference/list-of-unit-tags-supported-by-utterance-options.md) 문서에서 확인할 수 있습니다.

