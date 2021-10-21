# octagono-regular
Realice un programa en PHP que permita realzar el calculo del área de un octágono regular con valores dinámicos.

<?php

if(isset($_POST['btn']) && $_POST['btn'] == 'Calcular') {

	$lado = $_POST['lado'];
	$constante = 4.83;
	$area = 0;
	$ap= 0;

	if(isset($_POST['lado']) && !empty($_POST['lado'])) {

	$area = (($constante) * pow($lado, 2));
	$ap = ($area/(4*$lado));

		echo "<h2 align='center'>Resultados:</h2>";
		echo "<h2 align='center'>Longitud de los lados: " . $lado ."</h2>";
		echo "<h2 align='center'>Apotema del octagono: " . $ap ."</h2>";
		echo "<h2 align='center'>Area del octagono: " . $area ."</h2>";

		echo "<a href='index.html'>Volver atras</a>";
		unset($_POST['btn']);
		unset($_POST['lado']);

	} else {
	echo "<h2 align='center'>Resultados:</h2>";
	echo "<h2>No ha ingresado el valor de lado. Intentelo de nuevo</h2>";
	echo "<br/><br/>";
	echo "<a href='index.html'>Volver atras</a>";
	unset($_POST['btn']);
	unset($_POST['lado']);
	}

	} else{
		header('location: index.html');
	}
?>

<html>
	<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Área de un octágono regular</title>
	</head>
<body>
</body>
</html>
