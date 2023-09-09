<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ma Page d'Affiliation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 20px 0;
        }
        h1 {
            font-size: 36px;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            border-radius: 5px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            padding: 10px;
            text-align: center;
            border: 1px solid #ddd;
        }
        th {
            background-color: #333;
            color: #fff;
        }
        tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        a {
            text-decoration: none;
            color: #007bff;
            font-weight: bold;
        }
        #toggleLanguage {
            background-color: #007bff;
            color: #fff;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Liste de Produits Affiliés</h1>
        <button id="toggleLanguage" onclick="toggleLanguage()">Switch to English</button>
    </header>
    <div class="container">
        <table>
            <thead>
                <tr>
                    <th>Nom du Produit</th>
                    <th>Lien du Site</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td><a href="lien_affilie_produit1">Produit 1</a></td>
                </tr>
                <tr>
                    <td>2</td>
                    <td><a href="lien_affilie_produit2">Produit 2</a></td>
                </tr>
                <tr>
                    <td>3</td>
                    <td><a href="lien_affilie_produit3">Produit 3</a></td>
                </tr>
            </tbody>
        </table>
    </div>

    <script>
        function toggleLanguage() {
            const toggleButton = document.getElementById('toggleLanguage');
            const language = toggleButton.textContent === 'Switch to English' ? 'en' : 'fr';

            if (language === 'en') {
                document.documentElement.lang = 'en';
                toggleButton.textContent = 'Switch to French';
                document.querySelector('h1').textContent = 'Affiliate Product List';
                document.querySelector('th:nth-child(1)').textContent = 'Product Name';
                document.querySelector('th:nth-child(2)').textContent = 'Site Link';
                document.querySelector('button').textContent = 'Switch to French';
            } else {
                document.documentElement.lang = 'fr';
                toggleButton.textContent = 'Switch to English';
                document.querySelector('h1').textContent = 'Liste de Produits Affiliés';
                document.querySelector('th:nth-child(1)').textContent = 'Nom du Produit';
                document.querySelector('th:nth-child(2)').textContent = 'Lien du Site';
                document.querySelector('button').textContent = 'Switch to English';
            }
        }
    </script>
</body>
</html>

