<template>
    <div class="footer-dark">
      <footer>
          <div class="container">
                  <!-- <div class="col item social"><a href=https://github.com/kagopooe><span class="iconify" data-icon="akar-icons:github-outline-fill"></span></a><a href=mailto:kagopooe@gmail.com><i class="fa fa-at"></i></a><a href="https://twitter.com/kagopooe"><i class="fa fa-twitter"></i></a><a href="https://www.youtube.com/channel/UC1S71_9NjlEd2_1RnsMA1Hg"><i class="fa fa-youtube"></i></a></div> -->
              </div>
              <p class="copyright">© 2022 // Created by Kago Pooe</p>
      </footer>
  </div>
  
</template>

<script>
export default {

}
</script>

<style>
.footer-dark {
  padding: 50px 0;
  color: white;
  background-color: inherit;
}

.footer-dark .item.text {
  margin-bottom: 36px;
}

@media (max-width: 767px) {
  .footer-dark .item.text {
    margin-bottom: 0;
  }
}

.footer-dark .item.social {
  text-align: center;
}

@media (max-width: 991px) {
  .footer-dark .item.social {
    text-align: center;
    margin-top: 10px;
  }
}

.footer-dark .item.social > a {
  font-size: 20px;
  width: 36px;
  height: 36px;
  line-height: 36px;
  display: inline-block;
  text-align: center;
  border-radius: 50%;
  box-shadow: 0 0 0 1px white;
  margin: 0 8px;
  color: white;
  opacity: 0.75;
}

.footer-dark .item.social > a:hover {
  opacity: 0.9;
  color: #e2b921;
}

.footer-dark .copyright {
  text-align: center;
  padding-top: 24px;
  opacity: 0.3;
  font-size: 18px;
  margin-bottom: 0;
  color: white;
}

</style>