# QwertyToHebrew
Type in English QWERTY, instantly see correct Hebrew as if typed on Hebrew keyboard.

## Demo: https://il-internet.github.io/QwertyToHebrew/ 

Copy this and use it locally on your browser

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>QwertyToHebrew</title>
<style>
  body {font-family: Arial; padding: 20px;}
  div {min-height:50px; font-size:30px; font-weight:bold; color:#00c;}
  input {font-size: 24px; width: 100%; margin: 10px 0;}
</style>
</head>
<body>
<input id="inp" autocomplete="off">
<div id="out" dir="rtl"></div>
<script>
map = {
  'q': '/', 'w': '\'', 'e': 'ק', 'r': 'ר', 't': 'א', 'y': 'ט', 'u': 'ו', 'i': 'ן', 'o': 'ם', 'p': 'פ',
  'a': 'ש', 's': 'ד', 'd': 'ג', 'f': 'כ', 'g': 'ע', 'h': 'י', 'j': 'ח', 'k': 'ל', 'l': 'ך', ';': 'ף', "'": ',',
  'z': 'ז', 'x': 'ס', 'c': 'ב', 'v': 'ה', 'b': 'נ', 'n': 'מ', 'm': 'צ', ',': 'ת', '.': 'ץ', '/': '.',
  '`': '־', '[': ']', ']': '[', '-': '-', '=': '='
};
document.getElementById('inp').addEventListener('input', function(e) {
  val = e.target.value.toLowerCase();
  heb = '';
  for (ch of val) {
    heb += map[ch] || ch;
  }
  document.getElementById('out').textContent = heb;
});
</script>
</body>
</html>
```
