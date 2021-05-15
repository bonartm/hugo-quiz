# hugo-quiz

![build and deploy](https://github.com/bonartm/hugo-quiz/workflows/build%20and%20deploy/badge.svg)

> A hugo shortcode for writing quizzes with a markdown-like syntax, called [quizdown](https://github.com/bonartm/quizdown-js). 

### 🚀 See the [demo](https://bonartm.github.io/hugo-quiz/) based on the hugo learn theme or try the interactive [quizdown live editor](https://bonartm.github.io/quizdown-live-editor/).

- supports markdown text formatting, images and syntax highlighting.
- different [quiz-types](https://github.com/bonartm/quizdown-js/blob/main/docs/syntax.md): single-choice, multiple-choice, sequence.
- support for hints and explanations.
- [options](https://github.com/bonartm/quizdown-js/blob/main/docs/options.md) for color theme, question shuffling, localization.
- mobile friendly with touch support for all question types.


## Installation

1. Copy the content from `demo/layouts/shortcodes/quizdown.html`  into your local `layouts/shortcodes/` folder.
2. Add the `quizdown.js` to your project. For the hugo-learn theme you can copy the content of `demo/layouts/partials/custom-header.html` into your local `layouts/partials/` folder.

**Currently, the `--minify` flag of the hugo command causes issues with the raw quizdown-markdown code. Please remove the flag when building your website or use the following option in your `config.toml`**:

```toml
[minify]
  disableHTML = true
```


## Usage  (edit example in [🚀 quizdown editor](https://bonartm.github.io/quizdown-live-editor/?code=---%0Aprimary_color%3A%20orange%0Asecondary_color%3A%20lightgray%0Atext_color%3A%20black%0Ashuffle_questions%3A%20false%0A---%0A%0A%23%23%20The%20sound%20of%20dog%0A%0A---%0Ashuffle_answers%3A%20false%0A---%0A%0AWhat%20do%20dogs%20sound%20like%3F%0A%0A%3E%20Some%20hint%0A%0A-%20%5B%20%5D%20yes%0A-%20%5B%20%5D%20no%0A-%20%5B%20%5D%20%60self.sound%20%3D%20%22meow%22%60%0A-%20%5Bx%5D%20wuff%0A%0A%23%23%20Put%20the%20%5Bdays%5D(https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FDay)%20in%20order!%0A%0A%3E%20Monday%20is%20the%20*first*%20day%20of%20the%20week.%0A%0A1.%20Monday%0A2.%20Tuesday%0A3.%20Wednesday%0A4.%20Friday%0A5.%20Saturday%20))

Write quizzes in plain markdown in any of your files in the `content` directory:

```markdown

# Hugo Quiz

{{< quizdown >}}

---
primary_color: orange
secondary_color: lightgray
text_color: black
shuffle_questions: false
---

## The sound of dog

---
shuffle_answers: false
---

What do dogs sound like?

> Some hint

- [ ] yes
- [ ] no
- [ ] `self.sound = "meow"`
- [x] wuff

## Put the [days](https://en.wikipedia.org/wiki/Day) in order!

> Monday is the *first* day of the week.

1. Monday
2. Tuesday
3. Wednesday
4. Friday
5. Saturday  
{{< /quizdown >}}
```

## 📚 Documentation

> The quizzes are for fun and not for serious assessment. Since everything is rendered on the client side, the hints and solutions to the questions become visible once javascript is disabled in the browser.

Check out the [documentation](https://github.com/bonartm/quizdown-js/blob/main/docs/) on the main project page. You might be interested in:

- different [quiz-types](https://github.com/bonartm/quizdown-js/blob/main/docs/syntax.md): single-choice, multiple-choice, sequence.
- support for [hints and explanations](https://github.com/bonartm/quizdown-js/blob/main/docs/syntax.md#hints-and-comments).
- [options](https://github.com/bonartm/quizdown-js/blob/main/docs/options.md) for color theme, question shuffling, localization.

![](hugo-quiz-demo_v0.2.2.png)


## Demo

Tested with version `0.80.0` of Hugo and the Hugo Learn theme.

Visit https://bonartm.github.io/hugo-quiz/ for a live demo based on the [hugo-learn](https://themes.gohugo.io/theme/hugo-theme-learn/en) theme. You can also view a local version of the demo. 

First download the theme:

```shell
git submodule update --init --recursive
```

Then start the server:

```shell
cd demo
hugo server -D
```
