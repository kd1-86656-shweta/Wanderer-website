<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Local Storage Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }

        input {
            padding: 10px;
            margin: 10px;
        }

        button {
            padding: 10px;
            margin: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <h2>Local Storage Example</h2>

    <label for="data">Enter Data:</label>
    <input type="text" id="data" placeholder="Type something...">

    <button onclick="saveData()">Save Data</button>
    <button onclick="retrieveData()">Retrieve Data</button>

    <div id="result"></div>

    <script>
        function saveData() {
            const data = document.getElementById('data').value;
            localStorage.setItem('savedData', data);
            console.log(data); // corrected the typo here
            document.getElementById('result').textContent = 'Data saved!';
        }

        function retrieveData() {
            const savedData = localStorage.getItem('savedData');
            if (savedData) {
                document.getElementById('result').textContent = 'Retrieved Data: ' + savedData;
            } else {
                document.getElementById('result').textContent = 'No data found.';
            }
        }
    </script>

</body>
</html>
