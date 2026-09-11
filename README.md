<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Visualización Interactiva de la Fotosíntesis</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #e8f5e9, #c8e6c9);
      color: #183b20;
    }

    header {
      text-align: center;
      padding: 35px 20px;
      background: #2e7d32;
      color: white;
    }

    header h1 {
      margin: 0 0 10px;
      font-size: 32px;
    }

    header p {
      margin: 0;
      font-size: 17px;
    }

    .contenedor {
      max-width: 900px;
      margin: 30px auto;
      padding: 20px;
    }

    .tarjeta {
      background: white;
      border-radius: 20px;
      padding: 25px;
      margin-bottom: 25px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.12);
    }

    h2 {
      text-align: center;
      color: #2e7d32;
    }

    .controles {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .control {
      padding: 18px;
      border-radius: 15px;
      background: #f1f8e9;
    }

    .control label {
      display: block;
      font-weight: bold;
      margin-bottom: 8px;
    }

    select {
      width: 100%;
      padding: 11px;
      border-radius: 10px;
      border: 1px solid #aaa;
      font-size: 15px;
    }

    .proceso {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 15px;
      flex-wrap: wrap;
      margin: 30px 0;
    }

    .elemento {
      padding: 20px;
      border-radius: 18px;
      text-align: center;
      font-weight: bold;
      min-width: 150px;
    }

    .entrada {
      background: #fff8e1;
    }

    .hoja {
      background: #c8e6c9;
      border: 3px solid #43a047;
      transform: scale(1.05);
    }

    .salida {
      background: #e3f2fd;
    }

    .flecha {
      font-size: 35px;
      font-weight: bold;
    }

    #resultado {
      text-align: center;
      font-size: 26px;
      font-weight: bold;
      color: #2e7d32;
      margin: 20px 0 10px;
    }

    #explicacion {
      text-align: center;
      font-size: 17px;
      line-height: 1.5;
    }

    .ecuacion {
      text-align: center;
      background: #f1f8e9;
      padding: 20px;
      border-radius: 15px;
      font-size: 20px;
      font-weight: bold;
    }

    .pasos {
      line-height: 1.8;
      font-size: 17px;
    }

    footer {
      text-align: center;
      padding: 25px;
      background: #1b5e20;
      color: white;
      margin-top: 30px;
    }

    @media (max-width: 700px) {
      .controles {
        grid-template-columns: 1fr;
      }

      .flecha {
        transform: rotate(90deg);
      }

      header h1 {
        font-size: 25px;
      }
    }
  </style>
</head>

<body>

  <header>
    <h1>🌿 Visualización Interactiva de la Fotosíntesis</h1>
    <p>Observa cómo la luz, el agua y el CO₂ influyen en la fotosíntesis.</p>
  </header>

  <div class="contenedor">

    <div class="tarjeta">
      <h2>⚙️ Cambia las condiciones</h2>

      <div class="controles">

        <div class="control">
          <label>☀️ Luz solar</label>
          <select id="luz">
            <option value="1">Baja</option>
            <option value="2" selected>Media</option>
            <option value="3">Alta</option>
          </select>
        </div>

        <div class="control">
          <label>💨 Dióxido de carbono (CO₂)</label>
          <select id="co2">
            <option value="1">Bajo</option>
            <option value="2" selected>Medio</option>
            <option value="3">Alto</option>
          </select>
        </div>

        <div class="control">
          <label>💧 Agua</label>
          <select id="agua">
            <option value="1">Baja</option>
            <option value="2" selected>Media</option>
            <option value="3">Alta</option>
          </select>
        </div>

      </div>
    </div>

    <div class="tarjeta">

      <h2>🌱 ¿Cómo ocurre?</h2>

      <div class="proceso">

        <div class="elemento entrada">
          ☀️ Luz<br><br>
          💧 Agua<br><br>
          💨 CO₂
        </div>

        <div class="flecha">➜</div>

        <div class="elemento hoja">
          🌿<br>
          HOJA<br><br>
          Clorofila
        </div>

        <div class="flecha">➜</div>

        <div class="elemento salida">
          🍬 Glucosa<br><br>
          💨 Oxígeno
        </div>

      </div>

      <div id="resultado">
        Nivel de fotosíntesis: MEDIO
      </div>

      <p id="explicacion">
        La planta tiene condiciones moderadas para realizar la fotosíntesis.
      </p>

    </div>

    <div class="tarjeta">

      <h2>🧪 Ecuación de la fotosíntesis</h2>

      <div class="ecuacion">
        6 CO₂ + 6 H₂O + ☀️ → C₆H₁₂O₆ + 6 O₂
      </div>

    </div>

    <div class="tarjeta">

      <h2>📚 Proceso básico</h2>

      <div class="pasos">

        <p><strong>1. 💧 Absorción de agua:</strong> Las raíces absorben agua del suelo.</p>

        <p><strong>2. 💨 Entrada de CO₂:</strong> Las hojas toman dióxido de carbono del aire.</p>

        <p><strong>3. ☀️ Captación de luz:</strong> La clorofila de las hojas captura la energía de la luz solar.</p>

        <p><strong>4. 🍬 Producción de glucosa:</strong> La planta utiliza la energía para producir glucosa, que es su alimento.</p>

        <p><strong>5. 💨 Liberación de oxígeno:</strong> Como resultado del proceso, se libera oxígeno al ambiente.</p>

      </div>

    </div>

  </div>

  <footer>
    Visualización educativa sobre la fotosíntesis 🌱
  </footer>


  <script>

    const luz = document.getElementById("luz");
    const co2 = document.getElementById("co2");
    const agua = document.getElementById("agua");

    const resultado = document.getElementById("resultado");
    const explicacion = document.getElementById("explicacion");

    function actualizarFotosintesis() {

      const nivelLuz = Number(luz.value);
      const nivelCO2 = Number(co2.value);
      const nivelAgua = Number(agua.value);

      const nivel = Math.min(
        nivelLuz,
        nivelCO2,
        nivelAgua
      );

      if (nivel === 1) {

        resultado.textContent =
          "Nivel de fotosíntesis: BAJO";

        explicacion.textContent =
          "La fotosíntesis es limitada porque uno o más recursos se encuentran en un nivel bajo.";

      } else if (nivel === 2) {

        resultado.textContent =
          "Nivel de fotosíntesis: MEDIO";

        explicacion.textContent =
          "La planta tiene condiciones moderadas para realizar la fotosíntesis.";

      } else {

        resultado.textContent =
          "Nivel de fotosíntesis: ALTO";

        explicacion.textContent =
          "La planta dispone de suficiente luz, agua y CO₂ para realizar la fotosíntesis a un nivel alto.";

      }
    }

    luz.addEventListener("change", actualizarFotosintesis);
    co2.addEventListener("change", actualizarFotosintesis);
    agua.addEventListener("change", actualizarFotosintesis);

    actualizarFotosintesis();

  </script>

</body>
</html>
ve como se hace 
