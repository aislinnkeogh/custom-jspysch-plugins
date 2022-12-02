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
