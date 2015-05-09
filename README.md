$to = "cs.fauchetrotator@gmail.com" ;
$subject = "From Contact Us";
$nama = $_REQUEST['nama'] ;
$email = $_REQUEST['email'] ;
$phone = $_REQUEST['phone'] ;
$pesan = $_REQUEST['pesan'];
$headers = "From: $nama<$email>";
$message = "$pesan";
$sent = mail($to, $subject, $message, $headers) ;
if($sent)
{
?>
alert ('Thank You! Your message has been sent.');
window.location="http://bitcoinvo.blogspot.com/";
}
else
?>
alert ('Your message failed to be sent! Please try again.');
window.location="http://bitcoinvo.blogspot.com/";
?>
