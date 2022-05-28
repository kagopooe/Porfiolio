<template>
<div class="traineeship">
  <div class="process-row">
      <div class="activity animate-from-bottom__0">
          <div class="relative-block">
              <div class="activity-icon">
                  <img alt="An image" src="https://i.ibb.co/ZWp3Yts/ad-operations-process-strategy.png">
              </div>
              <div class="inactive">
                  <div class="title">Basic Calculator </div>
              </div>
              <div class="active">
                  <div class="title">Basic Calculator</div>
                  <div class="sub-title">Made a Calculator using Bootstrap and JavaScript. Used DOM manipulation to send data to the HTML and added code to give the calculator some functionality</div>
                  <div class="proj-links"><a href="https://flamboyant-leavitt-93419a.netlify.app/" target="_blank">Live</a>   //   <a href="https://github.com/kagopooe/Calculator" target="_blank">Code</a></div>
              </div>
          </div>
      </div>
      <div class="activity animate-from-bottom__1">
          <div class="relative-block">
              <div class="activity-icon">
                  <img alt="An image" src="https://i.ibb.co/s2nghrT/ad-operations-process-strategy-activation.png">
              </div>
              <div class="inactive">
                  <div class="title">Reaction Game </div>
              </div>
              <div class="active">
                  <div class="title">Reaction Game</div>
                  <div class="sub-title">Created a Reaction Game using a JavaScript Framework called Vue. The game measures the speed of the user's reaction time and reflexes in a simple manner</div>
                  <div class="proj-links"><a href="https://unruffled-hugle-da54c4.netlify.app/" target="_blank">Live</a>   //   <a href="https://github.com/kagopooe/reaction-game-vue" target="_blank">Code</a></div>

              </div>
          </div>
      </div>
      <div class="activity animate-from-bottom__2">
          <div class="relative-block">
              <div class="activity-icon">
                  <img alt="An image" src="https://i.ibb.co/ZWp3Yts/ad-operations-process-strategy.png">
              </div>
              <div class="inactive">
                  <div class="title">Pass Network</div>
              </div>
              <div class="active">
                  <div class="title">Football Team Pass Network Map</div>
                  <div class="sub-title">Created a Pass Network visualization using Python and Pandas to derive insights from a local mid-tier football club. I used coding tools to generate the raw data.</div>
                  <div class="proj-links"><a href="" target="_blank">Live</a>   //   <a href="https://github.com/kagopooe/pass-networks" target="_blank">Code</a></div>
              </div>
          </div>
      </div>
      <div class="activity animate-from-bottom__3">
          <div class="relative-block">
              <div class="activity-icon">
                  <img alt="An image" src="https://i.ibb.co/s2nghrT/ad-operations-process-strategy-activation.png">
              </div>
              <div class="inactive">
                  <div class="title">Data Manipulation</div>
              </div>
              <div class="active">
                  <div class="title">Data Filtering & Cleaning</div>
                  <div class="sub-title">Used a Python framework to extract pass information in order to gain specific data. The data was used to count a specific metric for a particular football team.
                  <div class="proj-links"><a href="" target="_blank">Live</a>   //   <a href="football-data-cleaning" target="_blank">Code</a></div>
            </div>
  
              </div>
          </div>
      </div>
      <div class="activity animate-from-bottom__4">
          <div class="relative-block">
              <div class="activity-icon">
                  <img alt="An image" src="https://i.ibb.co/ZWp3Yts/ad-operations-process-strategy.png">
              </div>
              <div class="inactive">
                  <div class="title">Pizza Chart</div>
              </div>
              <div class="active">
                  <div class="title">Football Player Statistics</div>
                  <div class="sub-title">Used R to scrape data and create a visualisation to analyse/measure the performance metrics of a professional footballer in a Pizza Plot.</div>
                  <div class="proj-links"><a href="" target="_blank">Live</a>   //   <a href="https://github.com/kagopooe/pizzacharts" target="_blank">Code</a></div>
              </div>
          </div>
      </div>
  </div><br>

    <div class="container-fluid more-proj">
         <p>
        <button class="btn more-proj-btn text-white" v-on:click=" collapsed = !collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#moreproj" aria-expanded="false" aria-controls="moreproj">
          More Projects  <div :class="[collapsed ? 'fa-chevron-down' : 'fa-chevron-up', 'fa']"></div>
        </button>
      </p><br>
      <div class="collapse" id="moreproj">
          <div class="traineeship">
  <div class="process-row">
      <div class="activity animate-from-bottom__0">
          <div class="relative-block">
              <div class="activity-icon">
                  <img alt="An image" src="https://i.ibb.co/ZWp3Yts/ad-operations-process-strategy.png">
              </div>
              <div class="inactive">
                  <div class="title">Will add soon sir </div>
              </div>
              <div class="active">
                  <div class="title">coming soon</div>
                  <div class="sub-title">placeholder</div>
                  <div class="proj-links"><a href="https://flamboyant-leavitt-93419a.netlify.app/" target="_blank">Live</a>   //   <a href="https://github.com/kagopooe/Calculator" target="_blank">Code</a></div>
              </div>
          </div>
      </div></div></div>






      </div>



    </div>




</div>


</template>

<script>
export default {
    data() {
        return{
    collapsed: true}
    
}
}
</script>

<style scoped>

.process-row {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
		justify-content: center;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    -ms-flex-direction: row;
    flex-direction: row;
    -webkit-box-pack: justify;
    -ms-flex-pack: justify;
    justify-content: space-between;
}
.traineeship .activity {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    width: 267px;
    margin: 15px 10px 10px;
    background-color: inherit;
    -webkit-box-shadow: 0 2px 6px 0 rgba(0, 0, 0, .1);
    box-shadow: 0 2px 6px 0 rgba(0, 0, 0, .1);
    /* cursor: pointer; */
    -webkit-transition: .3s;
    transition: .3s;
    overflow: hidden;
}
.animate-from-bottom__0 {
    -webkit-animation-name: from-left;
    animation-name: from-left;
    -webkit-animation-duration: .5s;
    animation-duration: .5s;
}
.animate-from-bottom__1 {
    -webkit-animation-name: from-left;
    animation-name: from-left;
    -webkit-animation-duration: .8s;
    animation-duration: .8s;
}
.animate-from-bottom__2 {
    -webkit-animation-name: from-left;
    animation-name: from-left;
    -webkit-animation-duration: 1s;
    animation-duration: 1s;
}
.animate-from-bottom__3 {
    -webkit-animation-name: from-left;
    animation-name: from-left;
    -webkit-animation-duration: 1.2s;
    animation-duration: 1.2s
}
.animate-from-bottom__4 {
    -webkit-animation-name: from-left;
    animation-name: from-left;
    -webkit-animation-duration: 1.2s;
    animation-duration: 1.2s
}
.traineeship .activity .relative-block {
    width: 100%;
    min-height: 350px;
}
@-webkit-keyframes from-left {
    from {
        -webkit-transform: translateY(50px);
        transform: translateY(50px)
    }

    to {
        -webkit-transform: translateX(0);
        transform: translateX(0)
    }
}
@keyframes from-left {
    from {
        -webkit-transform: translateY(50px);
        transform: translateY(50px)
    }

    to {
        -webkit-transform: translateX(0);
        transform: translateX(0)
    }
}
.relative-block {
    position: relative;
}
.activity-icon {
    position: absolute;
    bottom: 0;
    right: 0;
}
.activity-icon img {
    width: 70%;
    float: right;
}
.traineeship .inactive {
    padding: 20px;
}
.traineeship .inactive .title {
    border-bottom: 3px solid #f5ca2a;
    padding-bottom: 14px;
    width: -webkit-max-content;
    width: -moz-max-content;
    width: max-content;
    color:white;
    font-size: 1.2rem;
    font-weight: 400;
    line-height: 28px;
}
.traineeship .activity .active {
    display: none;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    -webkit-box-align: start;
    -ms-flex-align: start;
    align-items: flex-start;
    height: auto;
    min-height: 100%;
    padding: 25px 30px 50px;
}
.traineeship .activity .active .title {
    color: #1f1f1f;
    font-size: 22px;
    font-weight: 600;
    line-height: 32px;
}
.traineeship .activity .active .sub-title {
    margin-top: 10px;
    color: #616161;
    font-size: 16px;
    line-height: 28px;
    text-align: left;
}
.traineeship .activity .active .ul {
    margin-bottom: 45px;
    margin-top: 10px;
}
.traineeship .activity .active .li {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    margin-left: 30px;
    color: #616161;
    font-size: 16px;
    line-height: 26px;
}
.traineeship .activity .active .li:before {
    position: absolute;
    content: "\f00c";
    color: #e2b921;
    display: inline-block;
    margin-left: -1.6em;
    width: 22px;
}
.traineeship .activity:hover {
    width: 558px;
    background-color: #fff;
}
.traineeship .activity:hover .inactive {
    display: none;
}
.traineeship .activity:hover .active {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    width: 340px;
}

.proj-links {
    color: #616161;
    padding-top: 10px;
}

.proj-links a {
    color: #f5ca2a;
}

.more-proj p {
  text-align: center;
}

.more-proj-btn {
  background-color:#151415;
  box-shadow: none !important
}

@media only screen and (max-width: 1000px) {
    .process-row {
        flex-direction: column;
    }
    
    .traineeship .inactive .title{
        font-size: 1.5rem;
    }

    .traineeship .activity {
        width: 93%;
    }
    .traineeship .activity .active{
        width: 93%;
    }

    .traineeship .activity .active .sub-title {
        font-size: 1em;
        
    }

    .traineeship .activity .active .title {
        font-size: 1.2rem;
        font-weight: bold;
    }

    .traineeship .activity .relative-block {
        min-height: 100%;
    }

    .traineeship .activity:hover {
        width: 98%;
			margin-left:2px;
			margin-right:10px;
    }

}

@media only screen and (max-width: 400px){
    .activity-icon img {
        width: 30%;
    }
	    .traineeship .activity .active .sub-title {
        font-size: .7em;
        
    }
}

</style>



