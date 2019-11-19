# hugo-quiz

a custom hugo shortcode for interactive quizzes 


## Installation

- copy `item.html` and `quiz.html` into `layouts/shortcodes` folder
- copy `quiz.css` into `static/quiz.css` 
- copy `quiz.js` into `static/quiz.js`

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

Visit https://bonartm.github.io/hugo-quiz/ for a live demo.

## Credits

Quiz logic adopted from https://github.com/zimmicz/javascript-quiz-library
