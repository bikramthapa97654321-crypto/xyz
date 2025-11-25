<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3 Page Switch</title>
    <style>
        body{
            margin:0;
            font-family:Arial;
            background:#f2f2f2;
        }
        nav{
            background:#222;
            padding:15px;
            display:flex;
            gap:15px;
        }
        nav button{
            padding:10px 20px;
            border:none;
            background:#fff;
            cursor:pointer;
            border-radius:6px;
            font-weight:bold;
        }
        .page{
            display:none;
            padding:40px;
            background:white;
            margin:20px;
            border-radius:10px;
            box-shadow:0 0 10px rgba(0,0,0,0.1);
        }
        .active{
            display:block;
        }
    </style>
</head>
<body>
    <nav>
        <button onclick="showPage('p1')">Page 1</button>
        <button onclick="showPage('p2')">Page 2</button>
        <button onclick="showPage('p3')">Page 3</button>
    </nav>

    <div id="p1" class="page active">
        <h1>Page 1</h1>
        <p>This is the first page. Click buttons to switch.</p>
    </div>

    <div id="p2" class="page">
        <h1>Page 2</h1>
        <p>Welcome to the second page.</p>
    </div>

    <div id="p3" class="page">
        <h1>Page 3</h1>
        <p>You are now on page three.</p>
    </div>

    <script>
        function showPage(id){
            document.querySelectorAll('.page').forEach(pg => pg.classList.remove('active'));
            document.getElementById(id).classList.add('active');
        }
    </script>
</body>
</html>
