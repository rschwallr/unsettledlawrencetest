# unsettledlawrencetest
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Earth Project Viewer</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
            font-family: Arial, sans-serif;
        }
        .container {
            display: flex;
            flex-direction: column;
            height: 100vh;
        }
        .header {
            padding: 10px;
            background-color: #f8f9fa;
            text-align: center;
            border-bottom: 1px solid #ddd;
        }
        .content {
            flex: 1;
            position: relative;
        }
        iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        .loading {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="content">
            <div class="loading" id="loadingMessage">Loading Google Earth Project...</div>
            <iframe 
                src="https://earth.google.com/earth/d/1-Q_WzrCx0g6eLsHf52t34xdh_-ZZZTW-?usp=sharing&embed=true&presentation=true" 
                allowfullscreen
                onload="document.getElementById('loadingMessage').style.display='none';"
            ></iframe>
        </div>
    </div>
</body>
</html>
