---
title: "[Kramdown] Kramdown으로 랜더링되는 code 영역에 줄번호 표시하기"
category: [Kramdown, Jekyll, Markdown]
tag:
 - Kramdown
 - Jekyll
 - Markdown
 - Code
 - LineNumber
 - Highlight
 - Auto Wrapping
 - Warp
 - Auto
---

Jekyll로 구성된 웹페이지는 Markdown과 비슷한 Kramdown을 사용하는 경우가 많다. 기본적으로 Kramdown문법이 Markdown과 같아서 글을 작성하는데 어려움이 없고 Markdown보다 더 많은 기능을 제공한다. 코드를 표시할때 \`\`\`을 사용하여 표시한다. 이럴때 라인넘버가 나오지 않아서 긴 코드를 볼때 불편함이 많다. code영역에 라인 번호를 출력하는 방법에 대해서 알아본다.

# Code 영역에 라인 번호 출력하기

두 가지 방법으로 원하는 결과를 얻을 수 있다.

## _config.xml을 수정하는 방법

`_config.xml`에 아래의 내용을 넣는다.

```markdown
markdown: kramdown
kramdown:
  highlighter: rouge
  syntax_highlighter_opts:
    block:
      line_numbers: true
```

본문에서는 \`\`\`을 그대로 사용하면서 출력되는 내용에만 라인 번호를 표시할 수 있다.

## Kramdown의 code highlight를 사용하는 방법

코드블록 작성 시 위 코드의 맨 위와 아래에 아래의 코드를 사용한다.

```markdown
{ % highlight python linenos % }
code_contents
{ % endhighlight % }
```

기존에 Markdown으로 작성된 code영역을 모두 바꾸어 주어야 한다는 단점을 가지고 있다.

# 여담 : 라인 번호와 자동 줄바꿈 기능

코드에 라인 번호도 추가하였으니 자동 줄바꿈 기능도 탐이 날것이다. 하지만 라인 번호와 자동 줄바꿈은 같이 사용할 수 없다. 

`main.scss`에 아래의 코드를 추가하면 자동 줄바꿈 기능을 사용할 수 있다. 

```css
code.highlighter-rouge {
  white-space: pre-wrap;
}
```

하지만 이 기능은 최종적으로 jekyll 또는 kramdown/rouge 설정과 같이 사용되면 문제가 발생한다. 라인 번호는 `<td>`와 근처에 있는 `<td>`사이에 존재 하기 때문이다.

# 결론

다른 개발자가 코드를 잘 이해할 수 있도록 코드를 작성할때는 라인수도 적고 한화면을 넘어가지 않도록 글자수를 조절하는것이 당연하다. 따라서 코드를 작게 작성하는것이 가독성이 좋을수 있는 방법이다. 여러 함수를 표시하는 경우에는 각 함수들은 작지만 전체 코드의 라인수는 많아질 수 있다. 가로 줄을 줄이는것은 코드를 작성하는 사람의 몫으로 남기고 라인정보를 표시하면 개발자 사이에서 소통할때 라인 번호를 얘기하는것으로 충분한 소통이 될것이라고 생각하기 때문에 자동 줄바꿈 기능을 포기하고 라인 번호를 출력하는것을 선택하는것이 좋을것이다.

# 참고

* [How to display code blocks with word wrap and line number with jekyll markdown on github-pages](https://www.titanwolf.org/Network/q/173e9319-f67d-42be-ba86-5db4cc399ca3/y)
* [github code block에 line number 추가하기 ](https://helloyjam.github.io/github/markdown-code-linenumber/)
