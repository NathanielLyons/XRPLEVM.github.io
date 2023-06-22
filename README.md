<!DOCTYPE html>
<html>
<head>
  <title>Etherscan API</title>
</head>
<body>
  <form id="apiForm">
    <label for="address">Address:</label>
    <input type="text" id="address" name="address" required><br>

    <label for="contractAddress">Contract Address:</label>
    <input type="text" id="contractAddress" name="contractAddress" required><br>

    <label for="page">Page:</label>
    <input type="number" id="page" name="page" required><br>

    <label for="offset">Offset:</label>
    <input type="number" id="offset" name="offset" required><br>

    <label for="apiKey">API Key:</label>
    <input type="text" id="apiKey" name="apiKey" required><br>

    <button type="submit">Submit</button>
  </form>

  <div id="result"></div>

  <script>
    document.getElementById('apiForm').addEventListener('submit', function(event) {
      event.preventDefault(); // Prevent form submission

      var address = document.getElementById('address').value;
      var contractAddress = document.getElementById('contractAddress').value;
      var page = document.getElementById('page').value;
      var offset = document.getElementById('offset').value;
      var apiKey = document.getElementById('apiKey').value;

      var url = 'https://api.etherscan.io/api?module=account&action=addresstokennftinventory&address=' + address + '&contractaddress=' + contractAddress + '&page=' + page + '&offset=' + offset + '&apikey=' + apiKey;

      fetch(url)
        .then(function(response) {
          return response.json();
        })
        .then(function(data) {
          document.getElementById('result').textContent = JSON.stringify(data);
        })
        .catch(function(error) {
          console.log(error);
        });
    });
  </script>
</body>
</html>
