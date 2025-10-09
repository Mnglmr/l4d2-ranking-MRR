<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sistema de MMR - L4D2</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #1b1b1b;   /* Fondo general oscuro */
      color: #f0f0f0;
      margin: 0;
      padding: 0;
    }

    header {
      background: #27ae60;
      padding: 20px;
      text-align: center;
      font-size: 2em;
      font-weight: bold;
      color: #fff;
      box-shadow: 0 2px 5px rgba(0,0,0,0.5);
    }

    main {
      max-width: 900px;
      margin: 30px auto;
      background: #ffffff;          /* Fondo blanco para la tabla */
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.7);
    }

    h2 {
      text-align: center;
      color: #000000;               /* Título en negro */
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 10px;
      text-align: center;
      background: #ffffff;          /* Fondo de tabla blanco */
      color: #000000;               /* Texto de la tabla en negro */
    }

    th, td {
      padding: 12px;
      border-bottom: 1px solid #444;
      color: #000000;               /* Texto negro en las celdas */
    }

    th {
      background: #16a085;          /* Fondo verde para el encabezado */
      color: #ffffff;               /* Texto blanco para los encabezados */
      font-size: 1.1em;
    }

    tr:hover {
      background: #e6e6e6;          /* Efecto hover */
    }

    footer {
      text-align: center;
      padding: 10px;
      margin-top: 20px;
      color: #888;
      font-size: 0.9em;
    }
  </style>
</head>
<body>

  <header>Sistema de MMR - Left 4 Dead 2</header>

  <main>
    <h2>Clasificación de Jugadores</h2>
    <table id="mmrTable">
      <thead>
        <tr>
          <th>Jugador</th>
          <th>MMR</th>
        </tr>
      </thead>
      <tbody>
        <!-- Las filas se insertarán aquí mediante JavaScript -->
      </tbody>
    </table>
  </main>

  <footer>© 2025 Sistema MMR L4D2 - Fan Project</footer>

  <script>
    // Datos de los jugadores
    const jugadores = [
      { nombre: "Yasiel", mmr: 4198 },
      { nombre: "Kiba", mmr: 3960 },
      { nombre: "Manguito", mmr: 4114 },
      { nombre: "Holantau", mmr: 3717 },
      { nombre: "Adriel", mmr: 4902 },
      { nombre: "Joseph", mmr: 3176 },
      { nombre: "Fujimori", mmr: 3651 },
      { nombre: "Wyldtrak", mmr: 3330 },
      { nombre: "Vega", mmr: 3850 },
      { nombre: "Minyato", mmr: 4854 },
      { nombre: "Lala", mmr: 5855 },
       { nombre: "Yorka", mmr: 3659 },
    ];

    // Ordenar por MMR (de mayor a menor)
    jugadores.sort((a, b) => b.mmr - a.mmr);

    // Insertar los datos en la tabla
    const tbody = document.querySelector("#mmrTable tbody");

    jugadores.forEach((jugador) => {
      const row = document.createElement("tr");
      row.innerHTML = `
        <td>${jugador.nombre}</td>
        <td>${jugador.mmr}</td>
      `;
      tbody.appendChild(row);
    });
  </script>

</body>
</html>


