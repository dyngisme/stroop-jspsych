<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>一个 jsPsych 实验</title>
    <script src="https://www.naodao.com/public/experiment/libs/jspsych-7/jspsych.js"></script>
    <script src="https://www.naodao.com/public/experiment/libs/plugin/plugin-html-keyboard-response.js"></script>
    <link rel="stylesheet" href="https://www.naodao.com/public/experiment/libs/jspsych-7/css/jspsych.css">
  </head>
  <body></body>
  <script>
    // 在下面写下你的 JS 代码
    // 初始化 jsPsych
const jsPsych = initJsPsych();
// 创建一个名为 text_key_response 的插件
let text_key_response = {
  type: jsPsychHtmlKeyboardResponse,
  stimulus: "<p>Hello World!</p><p>按下空格键结束该屏</p>",
  choices: " ",
  response_ends_trial: true
};
// 创建一个名为 timeline 的时间线
// 其中包含了 text_key_response
let timeline = [text_key_response]
// 让 jsPsych 加载 timeline
jsPsych.run(timeline);
  </script>
</html>
