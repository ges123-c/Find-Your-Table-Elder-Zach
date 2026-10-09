# Find-Your-Table-Elder-Zach<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1">

<title>Elder Zach's 70th Birthday</title>

<style>

body {

  font-family: Arial, sans-serif;

  background: #f3f5fa;

  color: #18366f;

  text-align: center;

  margin: 0;

}

header {

  background: #123b82;

  color: white;

  padding: 35px 15px;

  border-bottom: 5px solid silver;

}

h1 { font-size: 27px; }

main {

  background: white;

  max-width: 440px;

  margin: 25px auto;

  padding: 25px;

  border-radius: 16px;

}

input, button {

  width: 100%;

  padding: 14px;

  margin-top: 12px;

  box-sizing: border-box;

  font-size: 17px;

  border-radius: 8px;

}

input { border: 1px solid #aaa; }

button {

  background: #123b82;

  color: white;

  border: 0;

  font-weight: bold;

}

#result { margin-top: 22px; font-size: 20px; }

</style>

</head>

<body>

<header>

  <h1>ELDER ZACH'S 70TH BIRTHDAY</h1>

  <p>70 Years of Grace, Love & Legacy</p>

</header>

<main>

  <h2>Find Your Table</h2>

  <p>Enter your name to find your table number and name.</p>

  <input id="guest" placeholder="Enter your name">

  <button onclick="findTable()">Find My Table</button>

  <div id="result"></div>

</main>

<script>

const guests = [

  // Guest assignments will be added here before publishing.

];

function findTable() {

  const name = document.getElementById('guest').value.trim().toLowerCase();

  const result = document.getElementById('result');

  const matches = guests.filter(g => g.name.toLowerCase() === name);

  if (matches.length === 1) {

    result.textContent = 'Table ' + matches[0].number + ' — ' + matches[0].table;

  } else if (matches.length > 1) {

    result.textContent = 'Please enter your full name.';

  } else {

    result.textContent = 'Name not found. Please check your spelling or ask the event team.';

  }

}

</script>

</body>

</html>
