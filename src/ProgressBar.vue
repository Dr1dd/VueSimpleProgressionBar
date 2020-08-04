<template>
  <div class ="progress-bar-container">
      <div class ="progress-bar" :style="{'width': progressPercent, backgroundColor: color}" :class ="['progress-bar--'+size ,{'progress-bar--rounded': rounded}]">
      </div>
  </div>
</template>

<script>

export default {
  name: 'ProgressBar',
  props:{
      rounded: {
        type: Boolean,
        default: false
      },
      color:{
        type: String,
        default: '#76ceff',
      },
      size: {
        type: String,
        default: "medium",
      }

  },
  data(){
      return{
          progressPercent: '0%',
      }
  },
  created() {
  window.addEventListener("scroll", this.calcScrollY);
  },
  destroyed() {
  window.removeEventListener("scroll", this.calcScrollY);
  },
  methods:{
      calcScrollY(){
          var y = Math.round(window.scrollY);
          var scrollMaxY = window.scrollMaxY || (document.documentElement.scrollHeight - document.documentElement.clientHeight)
          this.progressPercent =Math.round((y/scrollMaxY)*100) + '%'
      }
  }
}
</script>

<style>
.progress-bar-container{
    width: 100%;
    position: fixed;
}
.progress-bar{
    height: 100%;
    background-color: #76ceff;
    transition: 0.1s ease;
}
.progress-bar--small{
    height: 5px;
}
.progress-bar--medium{
    height: 7px;
}
.progress-bar--big{
    height: 10px;
}
.progress-bar--rounded{
    border-radius: 5px;
}

</style>
