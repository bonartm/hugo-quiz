# hugo-quiz

a custom [hugo shortcode](https://gohugo.io/content-management/shortcodes/#readout) for interactive quizzes 

[!](hugo-quiz-demo.png)


## Installation

Copy the content from `src` into your local hugo project folder. This project defines 2 shortcodes: `quiz.html` and `item.html`.


## Usage

Create quizzes as hugo shortcodes in any of your markdown files in the `content` directory

```markdown

Here is a simple example of a quiz, written in markdown using hugo shortcodes

{{% quiz test_quiz%}}

## Quiz header

{{< item question="What is Tom's name?" answer=2 choices="tim,tom,carl" >}}
{{< item question="What is the capital of Germany?" answer=2 choices="Cologne,Berlin,Hamburg" >}}
{{% /quiz %}}

Click on the `submit` button to see the result.
```

## Demo

Visit https://bonartm.github.io/hugo-quiz/ for a live demo based on the [hugo-learn](https://themes.gohugo.io/theme/hugo-theme-learn/en) theme.

## Credits

Quiz logic adopted from https://github.com/zimmicz/javascript-quiz-library
