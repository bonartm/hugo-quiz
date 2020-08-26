# hugo-quiz

A custom [hugo shortcode](https://gohugo.io/content-management/shortcodes/#readout) for interactive quizzes. See the demo [here](https://bonartm.github.io/hugo-quiz/).

## Installation

- Tested with version `0.57.2` of Hugo.
- Copy the content from `demo/shortcodes` and `demo/static/js` into your local hugo project folder.

## Usage

Create quizzes as hugo shortcodes in any of your markdown files in the `content` directory

```markdown

Here is a simple example of a quiz, written in markdown using hugo shortcodes

{{% quiz test_quiz%}}

## Quiz header

{{< item question="What is Tom's name?" answers="2" choices="tim,tom,carl" >}}
{{< item question="What is the capital of Germany?" answers="2" choices="Cologne,Berlin,Hamburg" >}}
{{< item question="Which number is larger 12?" answers="2,3" choices="5,13,183,1" >}}

{{% /quiz %}}

Click on the `submit` button to see the result.
```

![](hugo-quiz-demo.png)

## Demo

Visit https://bonartm.github.io/hugo-quiz/ for a live demo based on the [hugo-learn](https://themes.gohugo.io/theme/hugo-theme-learn/en) theme.

You can also view a local of version of the demo by typing:

```shell
cd demo
hugo server -D
```

## Credits

Initial quiz logic and styling adopted from https://github.com/zimmicz/javascript-quiz-library
