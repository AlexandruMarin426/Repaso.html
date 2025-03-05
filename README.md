[Ejercicio Repaso.zip](https://github.com/user-attachments/files/19095840/Ejercicio.Repaso.zip)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejercicios de CSS</title>
    <style>
        /* Ejercicio 1: Aplicar Estilos Básicos */
        body {
            background-color: lightgray;
            color: black;
            font-family: Arial, sans-serif;
        }

        p {
            color: blue;
        }

        h1 {
            margin: 20px;
            font-size: 30px;
        }

        div {
            border: 2px solid black;
        }

        /* Ejercicio 2: Selectores en CSS */
        .destacado {
            color: red;
        }

        #caja p {
            color: green;
            background-color: gray;
        }

        /* Ejercicio 3: Modelo de Caja */
        .box {
            width: 300px;
            height: 150px;
            background-color: yellow;
            border: 5px solid blue;
            padding: 10px;
            margin: 20px;
            text-align: center;
            line-height: 130px;
        }

        /* Ejercicio 4: Flexbox */
        .flex-container {
            display: flex;
            justify-content: space-around;
        }

        .flex-item {
            width: 100px;
            height: 100px;
            text-align: center;
            line-height: 100px;
            font-weight: bold;
        }

        .item1 { background-color: red; }
        .item2 { background-color: green; }
        .item3 { background-color: blue; }

        /* Ejercicio 5: Grid Layout */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-template-rows: 100px 200px;
            gap: 10px;
        }

        .grid-item {
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            font-weight: bold;
        }

        .itemA { background-color: lightcoral; }
        .itemB { background-color: lightblue; }
        .itemC { background-color: lightgreen; }
        .itemD { background-color: lightpink; }
        .itemE { background-color: lightgray; }
        .itemF { background-color: lightyellow; }

        /* Dashboard */
        .dashboard {
            display: flex;
            height: 100vh;
        }

        .sidebar {
            width: 20%;
            background-color: #333;
            color: white;
            padding: 20px;
        }

        .sidebar nav a {
            display: block;
            color: white;
            text-decoration: none;
            padding: 10px;
        }

        .sidebar nav a:hover {
            background-color: #555;
        }

        .header {
            width: 80%;
            background-color: darkgray;
            color: white;
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .main {
            width: 80%;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 200px);
            gap: 20px;
            padding: 20px;
        }

        .card {
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            font-weight: bold;
            transition: transform 0.3s ease, background-color 0.3s ease;
        }

        .card:nth-child(1) { background-color: lightblue; }
        .card:nth-child(2) { background-color: lightcoral; }
        .card:nth-child(3) { background-color: lightgreen; }
        .card:nth-child(4) { background-color: lightgoldenrodyellow; }

        .card:hover {
            transform: scale(1.1);
            background-color: gray;
        }

        /* Modo Oscuro */
        .dark-mode {
            background-color: black;
            color: white;
        }

        .dark-mode .header {
            background-color: #222;
        }

        .dark-mode .sidebar {
            background-color: #111;
        }

        .dark-mode .card {
            background-color: #444;
            color: white;
        }

        /* Responsividad */
        @media (max-width: 600px) {
            .main {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <h1>Bienvenidos a CSS</h1>
    <p class="destacado">Este es un párrafo destacado.</p>
    <p>Este es un párrafo normal.</p>

    <div id="caja">
        <p>Texto dentro de un div.</p>
    </div>

    <div class="box">Caja con modelo de caja</div>

    <div class="flex-container">
        <div class="flex-item item1">1</div>
        <div class="flex-item item2">2</div>
        <div class="flex-item item3">3</div>
    </div>

    <div class="grid-container">
        <div class="grid-item itemA">A</div>
        <div class="grid-item itemB">B</div>
        <div class="grid-item itemC">C</div>
        <div class="grid-item itemD">D</div>
        <div class="grid-item itemE">E</div>
        <div class="grid-item itemF">F</div>
    </div>

    <div class="dashboard">
        <aside class="sidebar">
            <nav>
                <a href="#">Inicio</a>
                <a href="#">Reportes</a>
                <a href="#">Configuración</a>
            </nav>
        </aside>

        <header class="header">
            <h1>Dashboard</h1>
            <button id="toggleDarkMode">Modo Oscuro</button>
        </header>

        <main class="main">
            <div class="card">Card 1</div>
            <div class="card">Card 2</div>
            <div class="card">Card 3</div>
            <div class="card">Card 4</div>
        </main>
    </div>

    <script>
        document.getElementById('toggleDarkMode').addEventListener('click', function () {
            document.body.classList.toggle('dark-mode');
        });
    </script>

</body>
</html>

