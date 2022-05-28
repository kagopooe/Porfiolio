<template>
    <div class="container-fluid testimonial-sec">
      <p id="btn-txt">
        <button class="btn text-white" v-on:click=" collapsed = !collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#test-sec" aria-expanded="false" aria-controls="test-sec">
          Testimonials  <div :class="[collapsed ? 'fa-chevron-down' : 'fa-chevron-up', 'fa']"></div>
        </button>
      </p><br>
        <div class="collapse" id="test-sec">
            <div class="card card-body card-bg">
            <div class="container-fluid">
                <div class="row skill-icons">
                    <div class="col-sm">
                         <div class="testimonial-card">
                            <div class="header">
                                <h3> Mugammad Breda</h3>
                                    <p>Classmate</p>
                            </div>
                            
                            <div class="body">    
                                <p>"Kago is a great colleague and shows much potential as a web
            developer. He is well spoken even though he is very reticent"</p>
                            </div>
    
                             <div class="footer">
                                <span><i class="fas fa-quote-right"></i></span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="col-sm">
                        <div class="testimonial-card">
                            <div class="header">
                                <h3> Nadeem Johnson</h3>
                                    <p>Classmate</p>
                            </div>
                            
                            <div class="body">    
                                <p>"Kago has an eye for design. From what I have observed, he is
            extremely focused and very attentive. He is a natural coder"</p>
                            </div>
    
                             <div class="footer">
                                <span><i class="fas fa-quote-right"></i></span>
                            </div>
                        </div>

                  
                    </div>

                    <div class="col-sm">
                        <div class="testimonial-card">
                            <div class="header">
                                <h3> Alex Sexwale</h3>
                                    <p>Lecturer</p>
                            </div>
                            
                            <div class="body">    
                                <p>"Kago is a talented individual who has good attention to detail. He
            has the potential to do great things."</p>
                            </div>
    
                             <div class="footer">
                                <span><i class="fas fa-quote-right"></i></span>
                            </div>
                        </div>

                  
                    </div>

                    <div class="col-sm">
                        <div class="testimonial-card">
                            <div class="header">
                                <h3> Jason Wandrag</h3>
                                    <p>Lecturer</p>
                            </div>
                            
                            <div class="body">    
                                <p>"Sometimes I Wdummy text of the printing and typesetting industry."</p>
                            </div>
    
                             <div class="footer">
                                <span><i class="fas fa-quote-right"></i></span>
                            </div>
                        </div>

                  
                    </div>

                    <div class="col-sm">
                        <div class="testimonial-card">
                            <div class="header">
                                <h3> Bron Villet</h3>
                                    <p>Student Co-ordinator</p>
                            </div>
                            
                            <div class="body">    
                                <p>"Sometimes I Wdummy text of the printing and typesetting industry."</p>
                            </div>
    
                             <div class="footer">
                                <span><i class="fas fa-quote-right"></i></span>
                            </div>
                        </div>

                  
                    </div>

                    <div class="col-sm">
                        <div class="testimonial-card">
                            <div class="header">
                                <h3> Godwin Dzvapatsva</h3>
                                    <p>Head of Department</p>
                            </div>
                            
                            <div class="body">    
                                <p>"Sometimes I Wdummy text of the printing and typesetting industry."</p>
                            </div>
    
                             <div class="footer">
                                <span><i class="fas fa-quote-right"></i></span>
                            </div>
                        </div>

                  
                    </div>
             




          </div>
        </div>
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

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

#btn-txt {
    text-align: center;
}

.testimonial-sec {
    position:relative; 
    margin-top:50px;
}

.body {
    padding:30px;
    text-align:left;
    position:relative;
}

.body::before {
    position:absolute;
    content:"";
    width:360px;
      height:50px;
     background-color:lighten(#000,2%);
      left:-5PX;
      top:-30px;
      transform:rotate(7deg);
}

.testimonial-sec button {
  background-color:#151415;
  box-shadow: none !important
}

.card-bg {
  background-color: inherit;
}

.testimonial-card {
    background-color:lighten(#000,2%);
    width:350px;
    /* height: 336px; */
    overflow:hidden;
    padding-top: 20px;
    border-bottom: 2.5px solid #e2b921;
}

.header{
    padding:30px 30px;
    text-align:right;
    background-color:lighten(#000,5%);
}

h3{
    color:#fff;
    margin-bottom:5px;
    text-transform:uppercase;
}

.header p {
    color: #e2b921;
    margin-bottom:20px;
}

.testimonial-card p {
    /* font-size:15px; */
    line-height:1.7;
    /* letter-spacing:1px; */
}

.footer {
    padding:0px 30px 0px 30px;
    text-align:right;
    position:relative;
}

.footer i {
    font-size:40px;
      position:absolute;
      bottom:6px;
      right:-5px;
}

.col-sm {
    padding-left: 50px;
}

.rotate {
    -moz-transition: all .5s linear;
    -webkit-transition: all .5s linear;
    transition: all .5s linear;
}
.rotate.down {
    -moz-transform:rotate(180deg);
    -webkit-transform:rotate(180deg);
    transform:rotate(180deg);
}

@media only screen and (max-width: 1102px) {
  .col-sm {
    /* margin-left: 20%; */
    display: flex;
justify-content: center;
  }
}

@media only screen and (max-width: 390px) {
  .col-sm {
    padding: 0;
    display: flex;
justify-content: center;
  }
}

</style>