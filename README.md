<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bienvenido!</title>
    <link rel="stylesheet" href="style.css">
</head> 
    <section>
    <div class="formulario">
     <h1>INGRESAR DATOS</h1>
        <form method="POST" action="registro.php">
		<div class="username">
                <input type="text" required>
                <label>Nombre</label>
            </div>
			<div class="username">
                <input type="text" required>
                <label>Apellido</label>
            </div>
			<div class="username">
                <input type="text" required>
                <label>E-mail</label>
            </div>
            <div class="username">
                <input type="text" required>
                <label>Nombre de Usuario</label>
            </div>
            <div class="username">
                <input type="password" required>
                <label>Contraseña</label>
            </div>
            <input type="submit" value="Iniciar">
            <div class="index">
                Ya tienes cuenta? <a href="index.php">Inicia sesion!</a>
            </div>
        </form>
    </section>
</div>  

  <section>

    <?php
    $con=mysqli_connect("localhost", "root","","azafran") or die ("ERROR DE CONEXION");
    ?>
    
</section>

    
    <?php
    if(isset($_POST['insert'])){
     $nombre=$_POST['nombre'];
     $apellido=$_POST['apellido'];
     $usuario=$_POST['usuario'];
     $pass=$_POST['pass'];
     $email=$_POST['email'];
     $insertar="INSERT INTO usuario (nombre, apellido, email, usuario,clave) VALUES ('$nombre', '$apellido', '$email', '$usuario','$pass')";
     $ejecutar= mysqli_query ($con, $insertar);
     if($ejecutar)
     {echo"<script>alert('insertado correctamente')</script>";}
    }

    ?>
    

</body>
</html>
