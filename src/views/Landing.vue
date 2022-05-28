<template>
<div class="landing">
    <div class="progress">
	<div class="progress--wpr">
		<div class="progress--bar"></div>
	</div>
</div>

<div class="content">
    <div class="header">
	    <h2>My Portfolio // Kago Pooe</h2>
      <h3>Aspiring Software Developer & Data Analyst</h3>
    </div><br>
    <hr><br>

    <Banner />

    <div class="container-fluid text-center about">
      <div class="row">
        <div class="col-sm-6">
          <img src="../assets/profile.png" class=""  alt="">
        </div>
        <div class="col-sm-6" id="about-text">
          <p class="">My name is Kago Pooe. I'm a 26 year old from Cape Town, South Africa. I have recently attended a coding bootcamp in Web Development which has
            improved and diversified my skill-set. I aim to upskill further as I explore the coding world. <br><br>
            
            The people closest to me would describe me as a very quiet and reserved individual. In my spare time, I enjoy
            reading, spending time outdoors and learning new skills. My motto for life is - Life is better than Non-Life, always! <br><br>

            I enjoy reading and learning about Data Science and Analysis. I find it to be fun, which I would like to pursue a career
            in this field. Sports is my niche, so I base all of my self-learning projects on it but my aim to be able to develop transferrable 
            data skills across all career fields. I also have the skills to become an entry level front-end or back-end web developer.
          </p><br>
        </div>
      </div>
    </div><hr><br>

    <div class="container-fluid skills">
      <p>
        <button class="btn skills-btn text-white" v-on:click=" collapsed = !collapsed"  type="button" data-bs-toggle="collapse" data-bs-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
          My Skills <div :class="[collapsed ? 'fa-chevron-down' : 'fa-chevron-up', 'fa']"></div>
        </button>
      </p><br>
      <div class="collapse skills-bg" id="collapseExample">
        <div class="card card-body card-bg">
          <div class="container-fluid">
            <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4 text-center skill-icons">
              <div class="col"><span title="HTML"><span class="iconify" data-icon="akar-icons:html-fill"></span></span>
              </div>
              <div class="col"><span title="CSS"><span class="iconify" data-icon="akar-icons:css-fill"></span></span>
              </div>
              <div class="col"><span title="MySQL"><span class="iconify" data-icon="simple-icons:mysql"></span></span>
              </div>
              <div class="col"><span title="JavaScript"><span class="iconify" data-icon="akar-icons:javascript-fill"></span></span>
              </div>
              <div class="col"><span title="VueJS"><span class="iconify" data-icon="akar-icons:vue-fill"></span></span>
              </div>
              <div class="col"><span title="Python"><span class="iconify" data-icon="akar-icons:python-fill"></span></span>
              </div>
              <div class="col"><span title="R"><span class="iconify" data-icon="carbon:logo-r-script"></span></span>
              </div>
              <div class="col"><span title="Tableau"><span class="iconify" data-icon="ion:logo-tableau"></span></span>
              </div>
          </div>
        </div>
        </div>
      </div>
    </div>

  <p>Here are are a few of my projects: </p><br>

  <Projects />
  
  <p style="padding-top:25px;">My links: </p>
  <div class="container-fluid text-center my-links">
    <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4">
    <div class="col"><span><a href="https://thrilling-pancreas-4d2.notion.site/Kago-Pooe-547161907deb4854a611d14b7ed958c6" target="_blank">CV/Resume</a></span></div>
    <div class="col"><span><a href="https://github.com/kagopooe" target="_blank">Github</a></span></div>
    <div class="col"><span><a href="https://public.tableau.com/app/profile/kago.pooe" target="_blank">Tableau Public</a></span></div>
    <div class="col"><span><a href="#" target="_blank">Blog</a></span></div>
  </div>
  </div><br>
  <hr>

  <Testimonials />
  <br>  <hr><br>
	
  <p>Feel free to touch base/get in contact with me</p><br><br>

  <Contact />

  <Footer /><br>

  <hr>


</div>
</div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

}

html,
body {
  scroll-behavior: smooth;
  background-color: #151415;
  height: 100%;
  max-width: 100%;
  overflow-x:hidden

}

.progress {
	position: fixed;
	top: 0; left: 0;
	z-index: 1;
	width: 100%;
  height: 4.5px;
  background-color: #151415;
  border-radius: 0%;
}
.progress--wpr {
	width: 100%;
	height: 4.5px;
  color: #151415;
  border-radius: 0%;
}
.progress--bar {
	height: 4.5px;
	background-color: white;
	width: 0%;
  border-radius: 0%;
}
.content {
	
	margin: 0;
	padding: 10px 10%;
  width: 100%;
  height: 100%;
}

p { 
	line-height: 24px;
}

.landing {
  background-color: #151415;
  top: 0;
  left: 0%;
}

.header h2 {
    padding-top: 20px;
}

.header h3 {
    font-style: italic;
    color: silver;
    /* margin-top: -5px; */
}

.about {
  font-size: 1rem;
  line-height: 1.6;
  padding-top: 50px;
}

/* .about img {


} */

#about-text {
  padding-top: 20px;
  
 
  
}

.skills-bg {
  background-color: inherit;
}

.skills-btn {
  background-color:#151415;
  box-shadow: none !important
}


.skill-icons {
  font-size: 80px;
}

.skills p {
  text-align: center;
}

.my-links {
  padding: 20px 0px 50px;
}
.my-links span {
    border-bottom: 3px solid #f5ca2a;
    padding-bottom: 7px;
}

.my-links a {
color: white;
text-decoration: none;
}

.my-links .col {
  padding-bottom: 20px;
}


</style>

<script>
import Banner from "../components/Banner.vue"
import Projects from "../components/Projects.vue"
import Testimonials from "../components/Testimonials.vue"
import Contact from "../components/Contact.vue"
import Footer from "../components/Footer.vue"

export default {
  data() {
    return {
      collapsed: true
    };
  },
  methods: {

  },
  components: {
    Banner:Banner,
    Projects:Projects,
    Testimonials:Testimonials,
    Contact:Contact,
    Footer:Footer
  },
  mounted() {
      document.addEventListener("DOMContentLoaded", function() {
	document.addEventListener("scroll", function() {
		getProgress();
	});

	function getProgress() {					
		var topPos = document.documentElement.scrollTop;
		// Alternatively, you can use document.body.scrollTop || document.documentElement.scrollTop;
		
		// Remaining left to scroll
		var remaining = document.documentElement.scrollHeight - document.documentElement.clientHeight;
		// scrollHeight is the measurement of the element's entire content, whether all the content is visible or not
		// clientHeight is the inner height of the element, including padding
		
		var percentage = (topPos / remaining) * 100;

		document.querySelector(".progress--bar").style.width = percentage + "%";
	}
});
  },
};
</script>