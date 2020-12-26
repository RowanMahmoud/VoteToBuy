<template>
  <div>
<div class="container">  
  <form id="contact" action="" method="post">
    <h1> <strong><b> Create your Brand</b></strong></h1>
    <img class="profile-pic" src="../assets/fashion-logo.jpg" />
<div class="upload-button "><b> Upload Your Brand Logo</b></div>
<input class="file-upload" type="file" accept="image/*"/>

    <fieldset>
      <input placeholder="Your Brand name" type="text" tabindex="1" required autofocus>
    </fieldset>
    <fieldset>
      <input placeholder="Email Address" type="email" tabindex="2" required>
    </fieldset>
    <fieldset>
      <input placeholder=" Password" type="tel" tabindex="3" required>
    </fieldset>
    <fieldset>
      <input placeholder=" Phone Number" type="tel" tabindex="4" required>
    </fieldset>
    <fieldset>
      <input placeholder="Facebook or Instgrame Link" type="url" tabindex="5" required>
    </fieldset>
    <fieldset>
      <textarea placeholder="About your Brand" tabindex="6" required></textarea>
    </fieldset>
    <router-link to="/brandprofile">
    <fieldset>
      <button name="submit" type="submit" id="contact-submit" data-submit="...Sending">Submit</button>
    </fieldset>
    </router-link>
  </form>
 
  
</div>

  </div>
</template>
<script>
    import $ from 'jquery';
    $("#slider > div:gt(0)").hide();
    setInterval(function () {
        $('#slider > div:first')
            .fadeOut(1000)
            .next()
            .fadeIn(1000)
            .end()
            .appendTo('#slider');
    }, 3000);
</script>
<script>
export default {

  data:function(){
  $(document).ready(function() {

    
    var readURL = function(input) {
        if (input.files && input.files[0]) {
            var reader = new FileReader();

            reader.onload = function (e) {
                $('.profile-pic').attr('src', e.target.result);
            }
    
            reader.readAsDataURL(input.files[0]);
        }
    }
    

    $(".file-upload").on('change', function(){
        readURL(this);
    });
    
    $(".upload-button").on('click', function() {
       $(".file-upload").click();
    });
});
}
}
</script>

<style lang="scss">
@import url(https://fonts.googleapis.com/css?family=Open+Sans:400italic,400,300,600);

* {
	margin:0;
	padding:0;
	box-sizing:border-box;
	-webkit-box-sizing:border-box;
	-moz-box-sizing:border-box;
	-webkit-font-smoothing:antialiased;
	-moz-font-smoothing:antialiased;
	-o-font-smoothing:antialiased;
	font-smoothing:antialiased;
	text-rendering:optimizeLegibility;
}
.upload-button  {
    padding: 4px;
    display: block;
    float: left;
    
}

.profile-pic {
    max-width: 300px;
    max-height: 200px;
    display: block;
}

.file-upload {
    display: none;
}

.container {
	max-width:400px;
	width:100%;
	margin:0 auto;
  position:relative;
  
}

#contact input[type="text"], #contact input[type="email"], #contact input[type="tel"], #contact input[type="url"], #contact textarea, #contact button[type="submit"] { font:400 12px/16px "Open Sans", Helvetica, Arial, sans-serif; }

#contact {
	background: #fadcda;
	padding:25px;
	margin:50px 0;
}

#contact h1 {
	color: -webkit-linear-gradient(#fadcda, #dc3545);
	display: block;
	font-size: 30px;
	font-weight: 400;
}

#contact h4 {
	margin:5px 0 15px;
	display:block;
	font-size:13px;
}

fieldset {
	border: medium none !important;
	margin: 0 0 10px;
	min-width: 100%;
	padding: 0;
	width: 100%;
}

#contact input[type="text"], #contact input[type="email"], #contact input[type="tel"], #contact input[type="url"], #contact textarea {
	width:100%;
	border:1px solid #CCC;
	background:#FFF;
	margin:0 0 5px;
	padding:10px;
}

#contact input[type="text"]:hover, #contact input[type="email"]:hover, #contact input[type="tel"]:hover, #contact input[type="url"]:hover, #contact textarea:hover {
	-webkit-transition:border-color 0.3s ease-in-out;
	-moz-transition:border-color 0.3s ease-in-out;
	transition:border-color 0.3s ease-in-out;
	border:1px solid #AAA;
}

#contact textarea {
	height:100px;
	max-width:100%;
  resize:none;
}

#contact button[type="submit"] {
	cursor:pointer;
	width:100%;
	border:none;
	background: #dc3545;
	color:#fadcda;
	margin:0 0 5px;
	padding:10px;
	font-size:20px;
}

#contact button[type="submit"]:hover {
	background:-webkit-linear-gradient(#fadcda, #dc3545);
	-webkit-transition:background 0.3s ease-in-out;
	-moz-transition:background 0.3s ease-in-out;
	transition:background-color 0.3s ease-in-out;
}

#contact button[type="submit"]:active { box-shadow:inset 0 1px 3px rgba(0, 0, 0, 0.5); }

#contact input:focus, #contact textarea:focus {
	outline:0;
	border:1px solid #999;
}
::-webkit-input-placeholder {
 color:#888;
}
:-moz-placeholder {
 color:#888;
}
::-moz-placeholder {
 color:#888;
}
:-ms-input-placeholder {
 color:#888;
}

</style>