<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Cuenta atrás boda</title>
<style>
  body {
    margin: 0;
    background: transparent;
    font-family: 'Arial', sans-serif;
    text-align: center;
    color: #2c2c2c;
  }

  .container {
    padding: 20px;
  }

  .title {
    font-size: 15px;
    letter-spacing: 2px;
    margin-bottom: 10px;
  }

  .subtitle {
    font-size: 10px;
    margin-bottom: 20px;
    opacity: 0.7;
  }

  .countdown {
    display: flex;
    justify-content: center;
    gap: 15px;
  }

  .time-box {
    border: 1px solid #ccc;
    padding: 8px 8px;
    min-width: 30px;
  }

  .number {
    font-size: 15px;
    font-weight: bold;
  }

  .label {
    font-size: 8px;
    letter-spacing: 1px;
    margin-top: 4px;
  }
</style>
</head>
<body>

<div class="container">
  <div class="title">CUENTA ATRÁS</div>
  <div class="subtitle">Para el día más importante de nuestras vidas</div>

  <div class="countdown">
    <div class="time-box">
      <div class="number" id="days">0</div>
      <div class="label">DÍAS</div>
    </div>
    <div class="time-box">
      <div class="number" id="hours">0</div>
      <div class="label">HORAS</div>
    </div>
    <div class="time-box">
      <div class="number" id="minutes">0</div>
      <div class="label">MINUTOS</div>
    </div>
    <div class="time-box">
      <div class="number" id="seconds">0</div>
      <div class="label">SEGUNDOS</div>
    </div>
  </div>
</div>

<script>
  const targetDate = new Date("2026-10-10T12:30:00").getTime();

  setInterval(() => {
    const now = new Date().getTime();
    const diff = targetDate - now;

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutes = Math.floor((diff / (1000 * 60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);

    document.getElementById("days").innerText = days;
    document.getElementById("hours").innerText = hours;
    document.getElementById("minutes").innerText = minutes;
    document.getElementById("seconds").innerText = seconds;
  }, 1000);
</script>

</body>
</html>
