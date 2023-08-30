# URL
web
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>URL Shortener</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
  }
  .container {
    max-width: 600px;
    margin: 2rem auto;
    padding: 2rem;
    background-color: #fff;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  }
  .input-field {
    width: 100%;
    padding: 0.5rem;
    margin-bottom: 1rem;
  }
  .button {
    padding: 0.5rem 1rem;
    background-color: #333;
    color: #fff;
    border: none;
    cursor: pointer;
  }
</style>
</head>
<body>
  <div class="container">
    <h2>URL Shortener</h2>
    <input type="url" class="input-field" id="longUrl" placeholder="Enter long URL">
    <button class="button" onclick="shortenURL()">Shorten</button>
    <p id="shortUrl"></p>
  </div>
  <script>
    function shortenURL() {
      const longUrl = document.getElementById('longUrl').value;
      const shortUrl = 'http://your-shortened-url.com/' + Math.random().toString(36).substring(7);
      document.getElementById('shortUrl').innerHTML = `<strong>Short URL:</strong> <a href="${shortUrl}" target="_blank">${shortUrl}</a>`;
    }
  </script>
</body>
</html>
