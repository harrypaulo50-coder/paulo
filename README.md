<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Glowing Flower</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  height: 100vh;
  background: radial-gradient(circle at bottom, #00111a, #000);
  overflow: hidden;
}

/* CONTAINER */
.container {
  position: relative;
  width: 100%;
  height: 100%;
}

/* FLOR */
.flower {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
}

/* HASTE */
.flower__line {
  width: 4px;
  height: 0;
  background: linear-gradient(to top, #0ff, transparent);
  margin: auto;
  animation: grow 2s ease forwards;
}

/* PÉTALAS */
.flower__petals {
  position: relative;
  width: 100px;
  height: 100px;
  margin: auto;
  margin-top: -20px;
}

.petal {
  position: absolute;
  width: 40px;
  height: 40px;
  background: #7df9ff;
  border-radius: 50%;
  box-shadow: 0 0 15px #7df9ff;
  opacity: 0;
  animation: bloom 2s ease forwards;
}

/* POSIÇÃO DAS PÉTALAS */
.petal:nth-child(1) { top: 0; left: 30px; animation-delay: 2s; }
.petal:nth-child(2) { top: 20px; left: 60px; animation-delay: 2.2s; }
.petal:nth-child(3) { top: 50px; left: 40px; animation-delay: 2.4s; }
.petal:nth-child(4) { top: 20px; left: 0px; animation-delay: 2.6s; }

/* CENTRO */
.center {
  position: absolute;
  top: 30px;
  left: 30px;
  width: 20px;
  height: 20px;
  background: #fff;
  border-radius: 50%;
  box-shadow: 0 0 20px #fff;
  opacity: 0;
  animation: bloom 2s ease forwards;
  animation-delay: 2.8s;
}

/* ANIMAÇÕES */
@keyframes grow {
  from {
    height: 0;
  }
  to {
    height: 200px;
  }
}

@keyframes bloom {
  from {
    transform: scale(0);
    opacity: 0;
  }
  to {
    transform: scale(1);
    opacity: 1;
  }
}
</style>
</head>

<body>
  <div class="container">
    <div class="flower">
      <div class="flower__line"></div>

      <div class="flower__petals">
        <div class="petal"></div>
        <div class="petal"></div>
        <div class="petal"></div>
        <div class="petal"></div>
        <div class="center"></div>
      </div>
    </div>
  </div>
