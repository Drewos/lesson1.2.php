<?php
error_reporting(-1);

$x = rand(0,100);
$num1 = 10;
$num2 = 20;


echo '<br>';

function checking(){
    global $x;
    global $num1;
    global $num2;

    $x_int = (int) $x;

    while($x_int <= $num1){
        echo 'Число ' .$x_int. '<br>';
        echo $num1 . '<br>';
        echo $num2 . '<br>';
        echo '<br>';

        if($num1 > $x_int){
            return 'Задуманное число не входит в числовой ряд' . '<br>';
        }

        else{
            if($num1 === $x_int){
                return 'Задуманное число входит в числовой ряд' . '<br>';
            }
            elseif($num1 !== $x_int){
                $num2 = $num1;
                $x_int = $x_int + $num1;
                $num1 = $num2;
            }
        }
    }   
}

echo checking();
