# index.html
Countdown
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Countdown to January 1, 2027</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 80px;
      background: #f4f4f4;
    }
    h1 {
      font-size: 2em;
    }
    #countdown {
      font-size: 1.5em;
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>

<h1>Countdown to January 1, 2027</h1>
<div id="countdown"></div>

<script>
function updateCountdown() {
  const targetDate = new Date("January 1, 2027 00:00:00").getTime();
  const now = new Date().getTime();
  const diff = targetDate - now;

  if (diff <= 0) {
    document.getElementById("countdown").innerHTML =
      "Judd Weaver is officially out of Kentucky politics.";
    return;
  }

  const days = Math.floor(diff / (1000 * 60 * 60 * 24));
  const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((diff % (1000 * 60)) / 1000);

  document.getElementById("countdown").innerHTML =
    `${days} days, ${hours} hours, ${minutes} minutes, ${seconds} seconds until Judd Weaver is officially out of Kentucky politics.`;
}

updateCountdown();
setInterval(updateCountdown, 1000);
</script>

</body>
</html>
