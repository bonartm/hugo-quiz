# hugo-quiz

A simple custom [hugo shortcode](https://gohugo.io/content-management/shortcodes/#readout) for basic interactive quizzes. See the demo [here](https://bonartm.github.io/hugo-quiz/).

These quizzes are for fun and not for serious assessment. Since everything is rendered on the client side, the hints and solutions to the questions are visible in the source code. 

## Installation

- Tested with version `0.80.0` of Hugo and the Hugo Learn theme. 
- Copy the content from `demo/shortcodes` and `demo/static/js` into your local hugo project folder.

## Usage

Create quizzes as hugo shortcodes in any of your markdown files in the `content` directory

```markdown

Here is a simple example of a quiz, written in markdown using hugo shortcodes

## Quiz header

{{< quiz test_quiz >}}

{{< item 
    question="What is Tom's name?" 
    answers="2" 
    choices="tim,tom,carl"
    hint="Tom's name is tom..." >}}
{{< item 
    question="What is the capital of Germany?" 
    answers="2" 
    choices="Cologne,Berlin,Hamburg"
    hint="The capital is Berlin" >}}
{{< item 
    question="Which number is larger 12?"
    answers="2,3" 
    choices="5,13,183,1"
    hint="Two numbers are larger!" >}}

{{< /quiz >}}

Click on the `submit` button to see the result.
```

![](hugo-quiz-demo.png)

## Demo

Visit https://bonartm.github.io/hugo-quiz/ for a live demo based on the [hugo-learn](https://themes.gohugo.io/theme/hugo-theme-learn/en) theme.

You can also view a local of version of the demo. First download the theme:

```shell
git submodule update --init --recursive
```

Then start the server:

```shell
cd demo
hugo server -D
```

## Credits

Initial quiz logic and styling adopted from https://github.com/zimmicz/javascript-quiz-library
