http class usage
======
use curl default , if curl is not installed , fsockopen method will be used.
	<?php
	require 'http.php';
	$http = new Http();
	//$http = new Http(array('timeout' => 10));
	//$http->method = 'POST';
	$http->timeout = 10;
	$http->target = 'http://www.google.com';
	/*
	$http->addParams(array(
		'username' => 'lzyy',
		'password' => '123456',
	));
	$http->addCookies(array(
		'foo' => 'bar',
	));
	//*/
	$http->execute();
	//echo $http->getResult();
	//echo $http->getHeaders();
	//echo $http->getStatus();

http_lite class useage
======
http_lite is a copy of kohana's remote class , curl is needed

	<?php
	echo remote::get('http://www.google.com');
