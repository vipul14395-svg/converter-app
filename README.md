# converter-app
ft to mm converter
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Feet to Millimeters Converter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 40px;
      background: #f4f4f9;
      color: #333;
    }
    h2 {
      color: #2c3e50;
    }
    input, button {
      padding: 10px;
      margin: 5px;
      font-size: 16px;
    }
    button {
      background: #3498db;
      color: white;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background: #2980b9;
    }
    #result {
      margin-top: 20px;
      font-weight: bold;
      font-size: 18px;
      color: #27ae60;
    }
  </style>
</head>
<body>
  <h2>Feet ➝ Millimeters Converter</h2>
  <input type="number" id="feet" placeholder="Enter value in feet">
  <button onclick="convert()">Convert</button>
  <div id="result"></div>

  <script>
    function convert() {
      let feet = document.getElementById("feet").value;
      if (feet === "") {
        document.getElementById("result").innerText = "Please enter a value!";
        return;
      }
      let mm = feet * 304.8;
      document.getElementById("result").innerText = feet + " ft = " + mm.toFixed(2) + " mm";
    }
  </script>
</body>
</html>
