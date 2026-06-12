<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Acceso</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:#000;
    color:white;
    font-family:Arial, sans-serif;
}

#login, #contenido{
    text-align:center;
}

input{
    padding:10px;
    font-size:16px;
    margin:10px;
}

button{
    padding:10px 20px;
    font-size:16px;
    cursor:pointer;
}

#contenido{
    display:none;
}

h1{
    font-size:60px;
    color:red;
    text-shadow:0 0 15px red;
}
</style>
</head>
<body>

<div id="login">
    <h2>Ingrese la contraseña</h2>
    <input type="password" id="clave" placeholder="Contraseña">
    <br>
    <button onclick="verificar()">Ingresar</button>
    <p id="mensaje"></p>
</div>

<div id="contenido">
    <h1>NO APTO PARA ZORRAS</h1>
</div>

<script>
function verificar(){
    const clave = document.getElementById("clave").value;

    if(clave === "1234"){
        document.getElementById("login").style.display = "none";
        document.getElementById("contenido").style.display = "block";
    }else{
        document.getElementById("mensaje").innerHTML = "Contraseña incorrecta";
        document.getElementById("mensaje").style.color = "red";
    }
}
</script>

</body>
</html>
