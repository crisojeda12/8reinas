<?php

	function Solucion($aux,$arreglo) 
	{
		for ($fila=0;$fila<$aux;$fila++) 
			{ 
				if ($arreglo[$fila] == $arreglo[$aux] || 
					($arreglo[$fila] - $arreglo[$aux]) == ($aux - $fila) ||
					($arreglo[$aux] - $arreglo[$fila]) == ($aux - $fila)) 
					return false;
			}
	return true;
	}

	function imprime_tablero($arreglo) 
	{

		for ($fila = 0; $fila < 8; $fila++) 
		{
			for ($columna = 0; $columna <8; $columna++) 
			{
				if ($arreglo[$fila] == $columna) 
						{echo("(".$fila.",".$columna.")	, ");}

			}
		}
	}
	function imprime_tablero2($arreglo) 
	{ 
		echo "</br>";
		for ($fila = 0; $fila <8; $fila++) 
		{
			for ($columna = 0; $columna <8; $columna++) 
			{
				if ($arreglo[$fila] == $columna) 
						echo("1  ");
				else echo("0  ");
			}
		echo '</br>';
		}
	echo '</br>';
	}
	function backtrack($aux,$arreglo) 
	{
		if ($aux == 8)//cuando las reinas ya sean 8
			{imprime_tablero($arreglo);//imprime las coordenadas
			imprime_tablero2($arreglo);}//imprime ggraficamente el tablero
		else 
		{
			for ($fila = 0; $fila <8; $fila++) 
			{
				$arreglo[$aux] = $fila;
				if (Solucion($aux,$arreglo)) //si es solucion entonces hace una recursion 
					backtrack($aux+1,$arreglo);//aumenta en uno el auxiliar en la recursion
			}

		}
	}

?>
<?php

$arreglo = Array();
 
backtrack(0,$arreglo);
 
?>
