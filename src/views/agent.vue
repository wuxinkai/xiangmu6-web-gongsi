<template>
   <div class="preloaderBox">
    <div id="preloader_1">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
    </div>
  </div>
</template>

<script>
import LoginMessage from '@/utils/sys_utils/agentTohome'
export default {
  created() {
    LoginMessage("home")
  }
}
</script>

<style>
.preloaderBox {
  height: 100%;
  width: 100%;
  background: #dfdfdf;
}
#preloader_1 {
  margin: 0 auto;
  position: absolute;
  top: 50%;
  left: 50%;
}
#preloader_1 span {
  display: block;
  bottom: 0px;
  width: 9px;
  height: 5px;
  background: #9b59b6;
  position: absolute;
  animation: preloader_1 1.5s infinite ease-in-out;
}
#preloader_1 span:nth-child(2) {
  left: 11px;
  animation-delay: 0.2s;
}
#preloader_1 span:nth-child(3) {
  left: 22px;
  animation-delay: 0.4s;
}
#preloader_1 span:nth-child(4) {
  left: 33px;
  animation-delay: 0.6s;
}
#preloader_1 span:nth-child(5) {
  left: 44px;
  animation-delay: 0.8s;
}
@keyframes preloader_1 {
  0% {
    height: 5px;
    transform: translateY(0px);
    background: #9b59b6;
  }
  25% {
    height: 30px;
    transform: translateY(15px);
    background: #3498db;
  }
  50% {
    height: 5px;
    transform: translateY(0px);
    background: #9b59b6;
  }
  100% {
    height: 5px;
    transform: translateY(0px);
    background: #9b59b6;
  }
}
</style>