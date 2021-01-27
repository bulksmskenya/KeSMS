# KeSMS
A simple Yii Framework text messaging solution for  Bulk SMS sending.  It aims at integration of  bulk sms API's with any web application that utilizes Kenyan telecom operators.




GETTING STARTED
---------------
  1. /assets - change permission to writable by webserver
  2. /protected/runtime - change permission to writable by webserver
  3. /uploads - change permission to writable by webserver
  4. /environment.php - add your absolute path to $local_path
  5. /index.php - define Yii Framework path to $local_path
  6. /protected/config/dbconnect.local.php - adjust configuration
  7. /protected/data/yiiopencms.sql - import database


  $partnerID = $app()->params["partnerId"];
  $apikey    = $app()->params["apiKey"];
  $shortcode = $app()->params["shortCode"];


  $finalURL = "{PROVIDER URL}/sendsms/?apikey=" {API KEY}"&partnerID=" {PARTNERID}"&message=" . {TEXT MESSAGE}. "&shortcode={CODE}&mobile={FONE}";
  $ch = curl_init();
  curl_setopt($ch, CURLOPT_URL, $finalURL);
  curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
  curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, false);
  $response = curl_exec($ch);
  curl_close($ch);
  //echo "Response: $response";
   return $response;

Demo Link
---------------

Demo: https://www.cabulksms.com/register

