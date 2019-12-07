<template>
  <div class="loader">加载中……</div>
</template>

<script>
  export default {
    name: "Loading"
  }
</script>

<style scoped>
  body{
    background: #56b4ab;
  }
  .loader {
    font-size: 10px;
    margin: 30% auto;
    text-indent: -9999em;
    width: 11em;
    height: 11em;
    border-radius: 50%;
    /* 线性渐变，从左到右，从白色到透明，0％代表起点和100％是终点 */
    background: linear-gradient(to right, #ffffff 10%, rgba(255, 255, 255, 0) 42%);
    position: relative;
    animation: load3 1.4s infinite linear;
  }
  .loader:before,
  .loader:after{
    content: '';
    position: absolute;
    top: 0;
    left: 0;
  }
  .loader:before {
    width: 50%;
    height: 50%;
    background: #FFF;
    border-radius: 100% 0 0 0;
  }
  .loader:after {
    background: #56b4ab;
    width: 75%;
    height: 75%;
    border-radius: 50%;
    margin: auto;
    bottom: 0;
    right: 0;
  }
  @keyframes load3 {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
</style>



