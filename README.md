# How to use these plugins

## `html-button-response-grid`

This plugin offers all the parameters from the built-in jsPsych `html-button-response` [plugin](https://www.jspsych.org/7.3/plugins/html-button-response/) as well as two new parameters: `rows` and `columns`.

The buttons defined in `choices` are displayed in a grid with dimensions `rows` x `columns` as specified by the user.

For example, the following code would generate a 2x2 (square) grid of images.

```
{
  type: jsPsychHtmlButtonResponseGrid,
  stimulus: "Click on the image described by the sentence below",
  choices: ["small_dog.png", "small_cat.png", "big_dog.png", "big_cat.png"],
  rows: 2,
  columns: 2,
  button_html: "<button class='jspsych-btn'> <img src='%choice%' width=500px></button>",
  prompt: "The big dog"
}
```

N.B. The plugin will throw an error if `rows * columns != choices.length`.

## `multiple-slider`

This plugin allows multiple slider inputs on one page in a slightly more aesthetically pleasing way than can be achieved with the built-in jsPsych survey plugins.

The `questions` parameter takes a list, each element of which gives the options for a single slider. The parameters for each question are similar to those offered by the built-in jsPsych `html-slider-response` [plugin](https://www.jspsych.org/7.3/plugins/html-slider-response/), with two key changes:

- `labels` no longer refers to the text that is displayed along the length of the slider, but rather to two labels that appear to the left of the slider: one above, and one below (I needed this for a specific use case, it can probably be ignored!)
- To set labels that show at equidistant locations along the slider, use the `ticks` parameter
