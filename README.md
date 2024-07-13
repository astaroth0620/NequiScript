<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NequiScriptxzz.com</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@100..900&display=swap');

        body {
            font-family: 'Roboto Slab', serif;
            text-align: center;
            background-color: #572354; /* Color uva */
            color: #FFF; /* Color blanco para el texto */
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 500px;
            margin: 10px auto; /* Centrado con margen superior e inferior de 10px */
            padding: 5px 10px; /* Reducción de 5px en la parte superior e inferior, y de 10px en los lados */
            background-color: #EFEFEF;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 7px; /* Reducido en 3px */
        }
        p {
            color: #333;
        }
        .input-field, .select-field {
            width: calc(100% - 22px); /* Ajusta para que esté dentro del margen */
            padding: 10px;
            margin: 10px auto; /* Centra el campo */
            border: 1px solid #CCC;
            border-radius: 5px;
            display: block;
        }
        .btn {
            padding: 10px 20px;
            background-color: #00B2E3;
            color: #FFF;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #008BB0;
        }
        .output {
            margin-top: 20px;
            font-size: 16px; /* Reducido en 0.2 */
            color: red;
        }
        .instagram {
            display: flex;
            align-items: center;
            justify-content: center; /* Alinea al centro */
            margin-top: 20px;
            flex-direction: column;
        }
        .instagram img {
            width: 35px; /* Aumentado en 0.7 */
            height: 35px; /* Aumentado en 0.7 */
            margin-right: 10px; /* Espacio entre logo y texto */
            margin-bottom: 0.2em; /* Bajado 0.2 */
        }
        .instagram p {
            color: #FFF; /* Color blanco */
            margin: 0;
        }
        .instagram a {
            color: #FFF; /* Blanco */
            text-decoration: none;
            font-weight: bold;
            font-size: 1em; /* Tamaño ajustado */
            text-decoration: underline;
            display: flex;
            align-items: center;
            margin-bottom: 0.2em; /* Bajado 0.2 */
        }
        .instagram a span {
            font-size: 1em; /* Tamaño ajustado */
            line-height: 0.8; /* Ajusta la altura de la línea */
            margin-top: 0.1em; /* Ajusta la separación */
            vertical-align: -0.4em; /* Ajusta la alineación vertical */
        }
        .title {
            font-family: 'Roboto Slab', serif;
            font-size: 3em; /* Tamaño del título */
            margin-top: 30px; /* Margen superior reducido */
            margin-bottom: 20px; /* Margen inferior */
            color: #572354; /* Color uva para el título */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="title">NequiScript</h1>
        <p>Busca cuentas de Nequi abandonadas con saldo y multiplica tu dinero!</p>
        <form id="nequiForm">
            <input type="text" id="nequiNumber" class="input-field" placeholder="Ingresa tu número Nequi" required>
            <select id="amount" class="select-field" required>
                <option value="">Selecciona el monto</option>
                <option value="80000">$80.000 recibes $300.000</option>
                <option value="100000">$100.000 recibes $450.000</option>
                <option value="180000">$180.000 recibes $600.000</option>
                <option value="250000">$250.000 recibes $800.000</option>
                <option value="300000">$300.000 recibes $1.000.000</option>
                <option value="500000">$500.000 recibes $1.800.000</option>
            </select>
            <button type="submit" class="btn">Buscar</button>
        </form>
        <div id="result" class="output"></div>
    </div>

    <footer>
        <div class="instagram">
            <p>Síguenos en nuestro Instagram:</p>
            <a href="https://instagram.com/santixzz06_1" target="_blank">
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram logo">
                @santixzz_1
            </a>
        </div>
    </footer>

    <script>
        document.getElementById('nequiForm').addEventListener('submit', function(event) {
            event.preventDefault();
            var nequiNumber = document.getElementById('nequiNumber').value;
            var amount = document.getElementById('amount').value;
            var resultDiv = document.getElementById('result');

            var nequiRegex = /^3\d{9}$/;
            if (!nequiRegex.test(nequiNumber)) {
                resultDiv.innerHTML = "No es una cuenta de Nequi";
                return;
            }

            if(nequiNumber && amount) {
                resultDiv.innerHTML = "¡Primero debes pagar para que tu cuenta de Nequi sea autorizada!";
            }
        });
    </script>
</body>
</html>
