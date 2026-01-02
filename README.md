<body> 

<?php 
$file_with_ips = 'ip.json'; 
$ips = file get_contents($file_with_ips); 
$contenido = json_decode($ips,true); 

if(isset($_get["mostrar"])){ 
echo "<p>ip: <b>".$contenido[$_GET["k"]] ."</b></p>"; 
else{ 
$contenido[$_get["k"]] = $_server[remote_addr]; file_put_contents($file_with_ips, json_encode($contenido));
}
  ?>
