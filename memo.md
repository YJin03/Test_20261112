지금 정리한 내용을 보면 마크다운의 기본 문법은 상당히 잘 공부하고 있어요! 특히 제목, 글자 꾸미기, 목록, 체크박스, 링크, 이미지, 표, 인용문, 코드 블록까지 다뤘네요.

다만 몇 가지 문법이 잘못 이해된 부분이 있고, GitHub README.md에서 사용할 때 알아두면 좋은 문법도 있어요.

지금 작성한 내용을 기준으로 부족한 부분과 추가로 공부하면 좋은 내용을 정리해 드릴게요.

# 1. 지금 작성한 내용 중 수정할 부분

## ① 굵게, 기울임, 취소선

| 기능       | 올바른 문법      | 결과   |
| -------- | ----------- | ---- |
| 굵게       | `**텍스트**`   | 텍스트  |
| 기울임      | `*텍스트*`     | 텍스트  |
| 굵게 + 기울임 | `***텍스트***` | 텍스트  |
| 취소선      | `~~텍스트~~`   | 텍스트  |
| 인라인 코드   | `` `코드` ``  | `코드` |

주의할 점

`**`와 `*`를 조합할 때는 다음처럼 사용하면 됩니다.

```
***굵게 기울임***
```

네가 작성한 굵게 + 기울임 문법은 조금 복잡하게 조합되어 있어요. 별표 3개를 사용하는 방법이 가장 간단합니다.

## ② 형광펜

작성한 문법:

```
<mark>형광펜</mark>
```

이것은 HTML 문법입니다.



정상 작동

&#x20;GitHub Markdown에서도 사용할 수 있습니다.



형광펜 효과

단, 모든 마크다운 플랫폼이 `<mark>`를 동일하게 지원하는 것은 아닙니다.

## ③ 목록의 차이점

작성한 내용에서 중요한 부분이에요.

```
- 목록
* 목록
+ 목록
```

세 가지 모두 순서 없는 목록을 만드는 문법입니다.

결과는 동일합니다.

- 마이너스(-)
- 별표(\*)
- 플러스(+)

들여쓰기를 사용하면 하위 목록을 만들 수 있습니다.

```
- 1단계
    - 2단계
        - 3단계
            - 4단계
```

\- 1단계

- 2단계
  - 3단계
    - 4단계

## ④ 순서 있는 목록

작성한 내용 중 숫자 부분은 조금 더 정확하게 이해하면 좋아요.

```
1. 사과
2. 바나나
3. 포도
4. 수박
```

실제 작성할 때는 숫자를 반드시 순서대로 적지 않아도 됩니다.

```
1. 사과
1. 바나나
1. 포도
1. 수박
```

렌더링 결과:

1. 사과
2. 바나나
3. 포도
4. 수박

즉, 마크다운은 숫자 자체보다 목록의 순서 구조를 인식합니다.

## ⑤ 체크박스

체크박스는 GitHub README에서 특히 유용합니다.

```
- [ ] 공부하기
- [x] 마크다운 정리하기
- [ ] README 작성하기
```

결과:

- 공부하기
- 마크다운 정리하기
- README 작성하기

`[ ]`는 미완료, `[x]`는 완료입니다.

## ⑥ 줄바꿈과 문단 구분

이 부분은 조금 헷갈릴 수 있어요.

| 작성 방법      | 기능                      |
| ---------- | ----------------------- |
| Enter 한 번  | 편집기 및 플랫폼에 따라 줄바꿈 처리 차이 |
| 빈 줄 추가     | 새로운 문단                  |
| 줄 끝에 공백 2개 | 같은 문단 내 줄바꿈             |
| `<br>`     | 강제 줄바꿈                  |

예시:

```
첫 번째 문장  
두 번째 문장

세 번째 문장
```

결과:

첫 번째 문장\
두 번째 문장

세 번째 문장

참고로 VS Code에서 Markdown 미리보기는 `Ctrl + Shift + V`로 열 수 있습니다.

# 2. 추가로 반드시 공부하면 좋은 문법

여기부터는 네가 아직 정리하지 않은 문법 위주입니다.

## ① 제목과 부제목

```
# 제목 1
## 제목 2
### 제목 3
#### 제목 4
##### 제목 5
###### 제목 6
```

실제 결과:

# 제목 1

## 제목 2

### 제목 3

#### 제목 4

#### 제목 5

#### 제목 6

주의할 점은 `#` 다음에 공백을 넣는 것입니다.

```
# 제목    (올바른 방식)
#제목     (일반적으로 제목으로 인식되지 않음)
```

## ② 구분선

네가 공부한 `---`, `___` 외에도 `***`를 사용할 수 있습니다.

```
---
***
___
```

결과:

구분선 앞뒤에는 빈 줄을 넣는 습관을 들이면 다른 문법과 충돌할 가능성이 줄어듭니다.

## ③ 인용문 (Blockquote)

인용문은 `>` 기호를 사용합니다.

```
> 첫 번째 인용
>> 두 번째 인용
>>> 세 번째 인용
```

결과:

> 첫 번째 인용
>
> > 두 번째 인용
> >
> > > 세 번째 인용

주로 참고 자료, 설명, 중요 내용 등을 강조할 때 사용합니다.

## ④ 링크 연결

네가 공부한 링크 문법에서 중요한 부분은 링크 이름과 URL을 구분하는 것입니다.

```
[네이버](https://naver.com)
```

결과: [네이버](https://naver.com?utm_source=chatgpt.com)

여기서 이미지에 링크를 연결하는 방법도 알아두세요.

```
[![이미지 설명](이미지URL)](이동할URL)
```

핵심 문법

이것이 네가 작성한 이미지 클릭 시 네이버로 이동하는 문법의 올바른 형태입니다.

## ⑤ 이미지 삽입

```
![이미지 설명](이미지URL)
```

예시:

[Minimalist Children Cute Characters Midjourney Prompt | PromptBase](https://images.openai.com/static-rsc-4/IhZ73ODEAbWySA9Lho-UjkU1tW-f3aRWU8wcaHndqj1748RONWAkyOxS9e9V8EGwvu00db_0oescdpve1JCA0j2dR7HVPMAHmzFx6CRZl2bDGB8xQCjFyCmuHqYjbuhK4qJja5nx2jj64ZeDLBh7oT-_FnlHdr91abHYN4cDlEg?purpose=inline)

```
![고양이 이미지](cat.png)
```

여기서 알아야 할 추가 개념이 있습니다.

- `cat.png`: 프로젝트 내부 이미지 파일
- `https://...`: 인터넷에 있는 이미지 주소
- `![]()`: 이미지를 표시하는 문법
- `[]()`: 링크를 표시하는 문법

## ⑥ 코드 블록

코드 블록은 백틱 3개를 사용합니다.

일반 코드:

````
```
코드 내용
```
````

언어 지정 코드:

````
```python
print("hello")
```
````

실제 결과:

```
print("hello")
```

언어를 지정하면 문법 강조(Syntax Highlighting)가 적용됩니다.

자주 사용하는 언어는 다음과 같습니다.

| 언어         | 지정 방법        |
| ---------- | ------------ |
| Python     | `python`     |
| JavaScript | `javascript` |
| HTML       | `html`       |
| CSS        | `css`        |
| SQL        | `sql`        |
| Bash       | `bash`       |
| JSON       | `json`       |

## ⑦ 표 만들기

표 문법도 잘 이해하고 있어요.

추가로 정렬 방법을 알아두면 좋습니다.

```
| 왼쪽 | 가운데 | 오른쪽 |
| :--- | :---: | ---: |
| 사과 | 바나나 | 포도 |
| 100 | 200 | 300 |
```

결과:

| 왼쪽 | 가운데 | 오른쪽 |
| -- | --- | --- |
| 사과 | 바나나 | 100 |
| 포도 | 수박  | 300 |

- `:---` 왼쪽 정렬
- `:---:` 가운데 정렬
- `---:` 오른쪽 정렬

## ⑧ HTML 문법 활용

마크다운에서 지원하지 않는 기능은 HTML을 일부 사용할 수 있습니다.

예를 들어:

```
<center>가운데 정렬</center>

<details>
<summary>자세히 보기</summary>

숨겨진 내용입니다.

</details>
```

실제 결과:

다만 `<center>`는 오래된 HTML 요소이므로 새로운 웹 문서에서는 CSS를 사용하는 것이 좋습니다. GitHub에서는 HTML 지원에도 제한이 있습니다.

## ⑨ 이모지 사용

GitHub에서는 이모지 단축 코드도 사용할 수 있습니다.

```
:smile:
:heart:
:fire:
:rocket:
:warning:
```

결과:

:smile: :heart: :fire: :rocket: :warning:

## ⑩ Mermaid 다이어그램

이건 꼭 추가로 공부해 보세요. 마크다운으로 순서도나 관계도를 그릴 수 있습니다.

````
```mermaid
flowchart TD
    A[공부 시작] --> B[마크다운 학습]
    B --> C[README 작성]
    C --> D[GitHub 업로드]
```
````

결과:

\#chatgpt-mermaid-\_r_cl\_{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;fill:rgb(13, 13, 13);}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#chatgpt-mermaid-\_r_cl\_ .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-\_r_cl\_ .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#chatgpt-mermaid-\_r_cl\_ .error-icon{fill:rgb(243, 243, 243);}#chatgpt-mermaid-\_r_cl\_ .error-text{fill:rgb(13, 13, 13);stroke:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ .edge-thickness-normal{stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ .edge-thickness-thick{stroke-width:3.5px;}#chatgpt-mermaid-\_r_cl\_ .edge-pattern-solid{stroke-dasharray:0;}#chatgpt-mermaid-\_r_cl\_ .edge-thickness-invisible{stroke-width:0;fill:none;}#chatgpt-mermaid-\_r_cl\_ .edge-pattern-dashed{stroke-dasharray:3;}#chatgpt-mermaid-\_r_cl\_ .edge-pattern-dotted{stroke-dasharray:2;}#chatgpt-mermaid-\_r_cl\_ .marker{fill:rgb(143, 143, 143);stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_cl\_ .marker.cross{stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_cl\_ svg{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:16px;}#chatgpt-mermaid-\_r_cl\_ p{margin:0;}#chatgpt-mermaid-\_r_cl\_ .label{font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ .cluster-label text{fill:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ .cluster-label span{color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ .cluster-label span p{background-color:transparent;}#chatgpt-mermaid-\_r_cl\_ .label text,#chatgpt-mermaid-\_r_cl\_ span{fill:rgb(13, 13, 13);color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ .node rect,#chatgpt-mermaid-\_r_cl\_ .node circle,#chatgpt-mermaid-\_r_cl\_ .node ellipse,#chatgpt-mermaid-\_r_cl\_ .node polygon,#chatgpt-mermaid-\_r_cl\_ .node path{fill:rgb(222, 234, 251);stroke:rgb(83, 154, 248);stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ .rough-node .label text,#chatgpt-mermaid-\_r_cl\_ .node .label text,#chatgpt-mermaid-\_r_cl\_ .image-shape .label,#chatgpt-mermaid-\_r_cl\_ .icon-shape .label{text-anchor:middle;}#chatgpt-mermaid-\_r_cl\_ .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ .rough-node .label,#chatgpt-mermaid-\_r_cl\_ .node .label,#chatgpt-mermaid-\_r_cl\_ .image-shape .label,#chatgpt-mermaid-\_r_cl\_ .icon-shape .label{text-align:center;}#chatgpt-mermaid-\_r_cl\_ .node.clickable{cursor:pointer;}#chatgpt-mermaid-\_r_cl\_ .root .anchor path{fill:rgb(143, 143, 143)!important;stroke-width:0;stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_cl\_ .arrowheadPath{fill:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_cl\_ .edgePath .path{stroke:rgb(143, 143, 143);stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ .flowchart-link{stroke:rgb(143, 143, 143);fill:none;}#chatgpt-mermaid-\_r_cl\_ .edgeLabel{background-color:rgb(252, 252, 252);text-align:center;}#chatgpt-mermaid-\_r_cl\_ .edgeLabel p{background-color:rgb(252, 252, 252);}#chatgpt-mermaid-\_r_cl\_ .edgeLabel rect{opacity:0.5;background-color:rgb(252, 252, 252);fill:rgb(252, 252, 252);}#chatgpt-mermaid-\_r_cl\_ .labelBkg{background-color:rgba(252, 252, 252, 0.5);}#chatgpt-mermaid-\_r_cl\_ .cluster rect{fill:rgb(243, 243, 243);stroke:rgba(0, 0, 0, 0.1);stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ .cluster text{fill:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ .cluster span{color:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";font-size:12px;background:rgb(243, 243, 243);border:1px solid rgba(0, 0, 0, 0.1);border-radius:2px;pointer-events:none;z-index:100;}#chatgpt-mermaid-\_r_cl\_ .flowchartTitleText{text-anchor:middle;font-size:18px;fill:rgb(13, 13, 13);}#chatgpt-mermaid-\_r_cl\_ rect.text{fill:none;stroke-width:0;}#chatgpt-mermaid-\_r_cl\_ .icon-shape,#chatgpt-mermaid-\_r_cl\_ .image-shape{background-color:rgb(252, 252, 252);text-align:center;}#chatgpt-mermaid-\_r_cl\_ .icon-shape p,#chatgpt-mermaid-\_r_cl\_ .image-shape p{background-color:rgb(252, 252, 252);padding:2px;}#chatgpt-mermaid-\_r_cl\_ .icon-shape .label rect,#chatgpt-mermaid-\_r_cl\_ .image-shape .label rect{opacity:0.5;background-color:rgb(252, 252, 252);fill:rgb(252, 252, 252);}#chatgpt-mermaid-\_r_cl\_ .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#chatgpt-mermaid-\_r_cl\_ .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#chatgpt-mermaid-\_r_cl\_ .node .neo-node{stroke:rgb(83, 154, 248);}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].node rect,#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].cluster rect,#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].node polygon{stroke:url(#chatgpt-mermaid-\_r_cl\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].swimlane.cluster rect{filter:none;}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].node path{stroke:url(#chatgpt-mermaid-\_r_cl\_-gradient);stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].node .outer-path{filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].node .neo-line path{stroke:rgb(83, 154, 248);filter:none;}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].node circle{stroke:url(#chatgpt-mermaid-\_r_cl\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].node circle .state-start{fill:#000000;}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].icon-shape .icon{fill:url(#chatgpt-mermaid-\_r_cl\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cl\_ [data-look="neo"].icon-shape .icon-neo path{stroke:url(#chatgpt-mermaid-\_r_cl\_-gradient);filter:drop-shadow( 1px 2px 2px rgba(185,185,185,1));}#chatgpt-mermaid-\_r_cl\_ .node text{font-size:14px;font-weight:600;letter-spacing:normal;fill:rgb(0, 79, 153);}#chatgpt-mermaid-\_r_cl\_ .edgeLabels text{font-size:13px;font-weight:600;letter-spacing:-0.08px;fill:rgb(0, 79, 153);}#chatgpt-mermaid-\_r_cl\_ .node tspan[font-weight="normal"],#chatgpt-mermaid-\_r_cl\_ .edgeLabels tspan[font-weight="normal"]{font-weight:600;}#chatgpt-mermaid-\_r_cl\_ .edgeLabel .label rect{opacity:1;rx:13px;ry:13px;fill:rgb(245, 250, 255);stroke:rgb(206, 219, 229);stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ .node rect,#chatgpt-mermaid-\_r_cl\_ .node circle,#chatgpt-mermaid-\_r_cl\_ .node ellipse,#chatgpt-mermaid-\_r_cl\_ .node polygon,#chatgpt-mermaid-\_r_cl\_ .node path{fill:rgb(229, 243, 255);stroke:rgba(0, 0, 0, 0.1);stroke-width:1px;}#chatgpt-mermaid-\_r_cl\_ .node rect{rx:16px;ry:16px;}#chatgpt-mermaid-\_r_cl\_ .mermaid-decision .label-container{fill:rgb(245, 250, 255);stroke:rgb(206, 219, 229);stroke-dasharray:2,2;}#chatgpt-mermaid-\_r_cl\_ .edgePaths .flowchart-link{stroke:rgb(143, 143, 143);stroke-width:1px;stroke-linecap:round;stroke-linejoin:round;}#chatgpt-mermaid-\_r_cl\_ .marker{fill:rgb(143, 143, 143);stroke:rgb(143, 143, 143);}#chatgpt-mermaid-\_r_cl\_ :root{--mermaid-font-family:-apple-system-body,ui-sans-serif,-apple-system,system-ui,"Segoe UI",Helvetica,"Apple Color Emoji",Arial,sans-serif,"Segoe UI Emoji","Segoe UI Symbol";}공부 시작마크다운 학습README 작성GitHub 업로드

# 3. 네가 공부한 내용에 추가할 마크다운 문법 요약

\| 문법 | 용도 | 중요도 |\
\|---|---|---|\
\| `**텍스트**` | 굵게 | 필수 |\
\| `*텍스트*` | 기울임 | 필수 |\
\| `~~텍스트~~` | 취소선 | 필수 |\
\| `# 제목` | 제목 | 필수 |\
\| `- 목록` | 순서 없는 목록 | 필수 |\
\| `1. 목록` | 순서 있는 목록 | 필수 |\
\| `- [ ]` | 체크박스 | 필수 |\
\| `[이름](URL)` | 링크 | 필수 |\
\| `![설명](URL)` | 이미지 | 필수 |\
\| `` `코드` `` | 인라인 코드 | 필수 |\
\| ` ```python ` | 코드 블록 | 필수 |\
\| `> 인용` | 인용문 | 추가 |\
\| `| 표 |` | 표 | 필수 |\
\| `<details>` | 접기/펼치기 | 추가 |\
\| `:smile:` | 이모지 | 추가 |\
\| `mermaid` | 다이어그램 | 추가 |\
\| `<mark>` | 형광펜 | 추가 |

# 4. 실전 연습 문제

지금까지 공부한 내용을 제대로 이해했는지 직접 연습해 보면 좋겠어요.

마크다운 기초 테스트

0/5 응답

Q1. 글자를 굵게 표시하는 올바른 문법은?

\*텍스트\*

\*\*텍스트\*\*

\~\~텍스트\~\~

Q2. 이미지를 삽입하는 문법은?

[이미지]\(URL)

![이미지]\(URL)

\#이미지(URL)

Q3. 순서 없는 목록을 만드는 기호가 아닌 것은?

\-

\*

\+

1\.

Q4. 같은 문단에서 강제로 줄을 바꾸는 방법은?

줄 끝에 공백 2개

빈 줄 추가

\# 기호

Q5. GitHub README에서 접기/펼치기에 사용하는 태그는?

\<mark>

\<details>

\<table>

채점하기

마지막 학습 추천: 지금은 마크다운 문법을 하나씩 외우는 것보다, 실제 GitHub 저장소에 `README.md` 파일을 만들어 제목, 표, 이미지, 링크, 코드 블록, 체크박스를 조합해서 하나의 문서를 완성해 보는 것을 추천해요.