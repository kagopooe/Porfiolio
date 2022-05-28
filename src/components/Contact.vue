<template>
<div id="section">

				<section class="contact-wrap">
				  <form action="https://formspree.io/f/mgerbjnz" method="POST" class="contact-form" id="my-form">
					<div class="col-sm-12">
					  <div class="input-block">
						<input type="text" class="form-control" name="fullname" placeholder="Full Name" required>
					  </div>
					</div>

					<div class="col-sm-12">
					  <div class="input-block">
						<input type="text" class="form-control" name="email" placeholder="Email Address" required>
					  </div>
					</div>
					<div class="col-sm-12">
					  <div class="input-block">
						<input type="text" class="form-control" name="subject" placeholder="Subject">
					  </div>
					</div>
					<div class="col-sm-12">
					  <div class="input-block textarea">
						<textarea rows="3" type="text" class="form-control" name="message" placeholder="Drop your message here" required></textarea>
					  </div>
					</div>
					<div class="col-sm-12">
					  <button class="square-button" type="submit">Send</button>
					</div>
				  </form>
          <div id="status"></div>
				</section>

</div>
</template>

<script>
export default {
  mounted() {
        var form = document.getElementById("my-form");
    
    async function handleSubmit(event) {
      event.preventDefault();
      var status = document.getElementById("status");
      var data = new FormData(event.target);
      fetch(event.target.action, {
        method: form.method,
        body: data,
        headers: {
            'Accept': 'application/json'
        }
      }).then(response => {
        if (response.ok) {
          status.classList.add('success');
          status.innerHTML = "Thanks! Message was sent successfully";
          form.reset()
        } else {
          response.json().then(data => {
            if (Object.hasOwn(data, 'errors')) {
              status.classList.add('errors')
              status.innerHTML = data["errors"].map(error => error["message"]).join(", ")
            } else {
              status.classList.add('error');
              status.innerHTML = "Oops! There was a problem submitting your form"
            }
          })
        }
      }).catch(error => {
        status.innerHTML = "Oops! There was a problem submitting your form"
      });
    }
    form.addEventListener("submit", handleSubmit)
  }



}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.wrap{
	width: 100%;
	height: 100%;
	margin-left: auto;
	margin-right: auto;
	position: relative;
}
.box{
	font-size: 1.2em;
	line-height: 1.6em;
  text-align: center;
}
/*screen resolutions lower than 620px*/
@media all and (max-width: 1180px){
	.wrap{
	width: 100%;
	height: 100%;
	margin-left: auto;
	margin-right: auto;
	position: relative;
	}
}


#section h2{
	margin-bottom: 50px;
  position: relative;
  display: block;
}
#section p a{
	color: #e2b921;
  text-decoration: none;
}
#section .wrap {
	text-align: center;
	width: 100%;
}
#section .box{
	text-align: center;
	margin: 5% 0 0 0;
	width: 100%;
}

.contact-form {
  width: 50%;
  margin: 0 auto;
  padding: 40px;
}
.contact-form .input-block {
  background-color: transparent;
  border: none;
  width: 100%;
  height: 60px;
  border-bottom: 2px solid white;
  margin: 0;
  position: relative;
  margin-bottom: 20px;
  -moz-transition: all 0.3s ease-out;
  -o-transition: all 0.3s ease-out;
  -webkit-transition: all 0.3s ease-out;
  transition: all 0.3s ease-out;
}

.contact-form .input-block.textarea {
  height: auto;
}
.contact-form .input-block.textarea .form-control {
  height: auto;
  resize: none;
}
.contact-form .input-block label {
  position: absolute;
  left: 10px;
  top: 25px;
  display: block;
  margin: 0;
  font-weight: 400;
  padding-top: 10px;
  z-index: 1;
  color: #aaa;
  font-size: 18px;
  line-height: 10px;
}
.contact-form .input-block .form-control {
  background-color: transparent;
  margin: 0;
  outline: none;
  border: none;
  -moz-border-radius: 0;
  -webkit-border-radius: 0;
  border-radius: 0;
  -moz-box-shadow: none;
  -webkit-box-shadow: none;
  box-shadow: none;
  height: auto;
    padding: 30px 10px;
  width: 100%;
  position: relative;
  z-index: 2;
  font-size: 18px;
  color: white;
}
.contact-form .input-block .form-control:focus label {
  top: 0;
}
.contact-form .square-button {
  background-color: #e2b921;
  color: #fff;
  font-size: 26px;
  text-transform: uppercase;
  font-weight: 700;
  text-align: center;
  -moz-border-radius: 2px;
  -webkit-border-radius: 2px;
  border-radius: 2px;
  -moz-transition: all 0.3s ease;
  -o-transition: all 0.3s ease;
  -webkit-transition: all 0.3s ease;
  transition: all 0.3s ease;
  padding: 0 60px;
  height: 60px;
  cursor: pointer;
  outline: none;
  border: none;
  width: 100%;
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
  -webkit-transition: all 0.3s ease-out;
  transition: all 0.3s ease-out;
}
.contact-form .square-button:hover, .contact-form .square-button:focus {
  background-color: #e2b921;
  box-shadow: 0px 10px 30px rgba(0,0,0,0.1);
  transform: translateY(-4px);
}

@media (min-width: 768px) {
  .contact-wrap {
    margin: auto;
  }
}
@media (max-width: 868px) {
	.contact-form {
	  width: 100%;
	  padding: 40px;
	}
}
@media (max-width: 568px) {
	.contact-form {
	  padding: 10px;
	}
}
/*----page styles---*/

.contact-wrap {
  padding: 15px;
  background: inherit;
}
.contact-wrap h1 {
  background-color: white;
  color: #ff7c62;
  padding: 40px;
  margin: 0 0 50px;
  font-size: 30px;
  text-transform: uppercase;
  font-weight: 700;
  text-align: center;
}
.contact-wrap h1 small {
  font-size: 18px;
  display: block;
  text-transform: none;
  font-weight: 300;
  margin-top: 10px;
  color: #ff7c62;
}

::placeholder {
  padding-bottom: 10px;
}

#status {
  width: 90%;
  max-width: 261px;
  text-align: center;
  padding: 10px;
  margin: 0 auto;
  border-radius: 8px;
}

#status.success{
  background-color: rgb(211,250,153);
  color: black;
  animation: status 6s ease forwards;
}

#status.error{
  background-color: rgb(250,129,92);
  animation: status 6s ease forwards;
}

#status.errors {
  background-color: rgb(250,129,92);
  animation: status 6s ease forwards;

}

@keyframes status {
  0% {
    opacity: 1;
    pointer-events: all;
  }
  90% {
    opacity: 1;
    pointer-events: all;
  }
  100% {
    opacity: 0;
    pointer-events: none;
  }
}


</style>