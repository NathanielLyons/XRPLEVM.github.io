# XRPLEVM.github.io
XRPL EVM SIDECHAIN INDEXER
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

  <script src="your-script.js"></script>
</body>
</html>
