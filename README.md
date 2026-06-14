<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Japanese Dictionary</title>

<style>
body {
  font-family: Arial, sans-serif;
  background: #f7f8fb;
  padding: 24px;
  color: #222;
}

h1 {
  text-align: center;
  color: #1f5bd8;
}

table {
  width: 100%;
  border-collapse: collapse;
  background: white;
}

th, td {
  padding: 16px;
  border-bottom: 1px solid #e5e5e5;
  text-align: left;
}

th {
  color: #1f5bd8;
}

.japanese {
  font-size: 26px;
  font-weight: bold;
}

button {
  background: #eaf1ff;
  border: none;
  border-radius: 50%;
  width: 46px;
  height: 46px;
  font-size: 20px;
}
</style>
</head>

<body>

<h1>Japanese Dictionary</h1>

<table>
<tr>
  <th>Audio</th>
  <th>Japanese</th>
  <th>Romaji</th>
  <th>English</th>
</tr>

<tr>
  <td><button onclick="speak('こんにちは')">▶</button></td>
  <td class="japanese">こんにちは</td>
  <td>konnichiwa</td>
  <td>hello</td>
</tr>

<tr>
  <td><button onclick="speak('ありがとう')">▶</button></td>
  <td class="japanese">ありがとう</td>
  <td>arigatou</td>
  <td>thank you</td>
</tr>

<tr>
  <td><button onclick="speak('すみません')">▶</button></td>
  <td class="japanese">すみません</td>
  <td>sumimasen</td>
  <td>excuse me / sorry</td>
</tr>

<tr>
  <td><button onclick="speak('お願いします')">▶</button></td>
  <td class="japanese">お願いします</td>
  <td>onegaishimasu</td>
  <td>please</td>
</tr>

<tr>
  <td><button onclick="speak('おはようございます')">▶</button></td>
  <td class="japanese">おはようございます</td>
  <td>ohayou gozaimasu</td>
  <td>good morning</td>
</tr>

</table>

<script>
function speak(text) {
  const utterance = new SpeechSynthesisUtterance(text);
  utterance.lang = "ja-JP";
  utterance.rate = 0.85;
  speechSynthesis.cancel();
  speechSynthesis.speak(utterance);
}
</script>

</body>
</html>