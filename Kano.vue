<template>
  <div>
    <iframe id="kano" title="Kano" allow="geolocation *" allowfullscreen frameBorder="0" :style=cssStyle :src=source></iframe>
  </div>
</template>

<script>
export default {
  name: 'kano',
  props: {
    source: {
      type: String,
      default: 'https://kano.dev.kalisio.xyz'
    },
    token: {
      type: String,
      default: ''
    },
    cssStyle: {
      type: String,
      default: 'width: 100%; height: 50vh'
    }
  },
  mounted () { 
    // see: https://vuepress.vuejs.org/guide/using-vue.html#browser-api-access-restrictions
    const kano = document.getElementById('kano').contentWindow 
    if (typeof postRobot === 'undefined') {
      let postRobotScript = document.createElement('script')
      postRobotScript.setAttribute('src',"https://cdn.jsdelivr.net/npm/post-robot@10.0.42/dist/post-robot.min.js")
      postRobotScript.onload = () => {
			  postRobot.on('kano-ready', () => {
          if (this.token !== '') {
            postRobot.send(kano, 'setLocalStorage', { 'kano-jwt': this.token })
          }
        })
      }
      document.head.appendChild(postRobotScript)
    }
  }
}
</script>
