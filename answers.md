

// 2 Question
$word="Join with storybox";
$parts = explode(' ', $word);
foreach ($parts as &$value) {
	$first=substr($value,0,1);
	$word_minus=substr($value,1);
	$end="ay";
	$regex="^(A|a|E|e|I|i|O|o|U|u)";
	if (preg_match("/$regex/", $word)) {
	echo $word.$end;
	echo " ";
	}
	else {
	echo $word_minus.$first.$end;
	echo " ";
	}
}

//3rd 
$arr = array(1,2,3,4,5,6,7); 
$n = sizeof($arr); 
rotate($arr, 2, $n);
function rotateone(&$arr, $n) 
{ 
    $temp = $arr[0]; 
    for ($i = 0; $i < $n - 1; $i++) 
        $arr[$i] = $arr[$i + 1]; 
    $arr[$i] = $temp;
} 
function rotate(&$arr, $d, $n) 
{ 
	for ($i = 0; $i <$d; $i++)
		rotateone($arr, $n)	;
		for ($i = 0; $i < $n; $i++) 
        echo $arr[$i] . " ";
}
