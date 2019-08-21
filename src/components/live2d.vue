<template>
  <!-- <div class="page">
      <h4>模型加载可能会慢</h4>
<div class="radio-container"></div>
<div class="url-container">
  <p>模型 cdn 地址</p>
  <p id="url"></p>
</div> -->

<div class="model-container">
  <canvas
    width="280"
    height="500"
    id="model"></canvas>
</div>
  <!-- </div> -->
</template>

<script>
  export default {
    data () {
      return {

      }
    },
    components: {

    },
    methods: {

    },
    computed: {

    },
    mounted(){
        //原js
/* const radioContainer = document.querySelector('.radio-container')
  const urlSpan = document.querySelector('#url')
  const prefix = 'live2d-widget-model-'
  const cdnPrefix = 'https://cdn.jsdelivr.net/gh/QiShaoXuan/live2DModel@1.0.0'
  const model = ['chitose',
    'epsilon2_1',
    'gf',
    'haru-01',
    'haru-02',
    'haruto',
    'hibiki',
    'hijiki',
    'izumi',
    'koharu',
    'miku',
    'ni-j',
    'nico',
    'nietzsche',
    'nipsilon',
    'nito',
    'shizuku',
    'tororo',
    'tsumiki',
    'unitychan',
    'wanko',
    'z16',]

  const radioHtml = model.reduce(((last, current) => last + `<label for="${current}"><input type="radio" id="${current}" name="modelName" class="modelRadio" value="${current}">${current}</label>`), '')

  radioContainer.innerHTML = radioHtml
  const radios = document.querySelectorAll('.modelRadio')


  radios.forEach((dom) => {
    dom.addEventListener('change', function () {

      let dir = ''
      console.log(this.value)

      switch (this.value) {
        case 'gf':
          dir = `/${prefix}${this.value}/assets/Gantzert_Felixander.model.json`
          break
        case 'epsilon2_1':
          dir = `/${prefix}${this.value}/assets/Epsilon2.1.model.json`
          break
        case 'haru-01':
          dir = `/live2d-widget-model-haru/01/assets/haru01.model.json`
          break
        case 'haru-02':
          dir = `/live2d-widget-model-haru/02/assets/haru02.model.json`
          break
        case 'ni-j' :
          dir = `/${prefix}${this.value}/assets/ni-j.model.json`
          break
        default:
          dir = `/${prefix}${this.value}/assets/${this.value}.model.json`
      }

      const url = cdnPrefix + dir
      urlSpan.innerText = url
      loadlive2d("model", url);
    })
  }) */

// 把${this.value}改成model里的就可以了
// 'gf'，'epsilon2_1'，'haru-01'，'haru-02'，'ni-j'比较特殊要额外的句子，上面也有
// let dir = `/live2d-widget-model-${this.value}/assets/${this.value}.model.json`

let dir = `/live2d-widget-model-wanko/assets/wanko.model.json`
const url = 'https://cdn.jsdelivr.net/gh/QiShaoXuan/live2DModel@1.0.0' + dir
loadlive2d("model", url);

    },
  }
</script>

<style scoped lang="scss" type="text/scss">
label {
    display: block;
    cursor: pointer;
  }

  input[type="radio"] {
    margin-right: 15px;
  }

  #model {
    position: fixed;
    right: 0px;
    bottom: 0;
    z-index: 99999;
    pointer-events: none;
  }

  .url-container {
    position: fixed;
    right: 10px;
    top: 15px;
  }

  .radio-container{
    width: 400px;
  }
 
</style>
