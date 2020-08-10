<template>
  <div class="body">
      <p>按住录制音频</p>
      <img src="../../static/image/timg.gif" alt="" @click="translationStart" >
      <span @click="translationStart">停止</span>
  </div>
</template>

<script>
import IatRecorder  from '@/assets/js/IatRecorder.js'

// import TransWorker from '../../../assets/js/transcode.worker.js'
import Enc from 'enc'
import VConsole from 'vconsole'

// let transWorker = new TransWorker()
// console.log(transWorker)
const iatRecorder = new IatRecorder('en_us','mandarin','5f27b6a9')//

export default {
  data() {
    return {
    };
  },
  mounted() {

  },
  created() {},
  methods: {

    translationStart(){
  
            iatRecorder.start()
 
    },
    translationEnd(){
      iatRecorder.stop()
    }
  },
};
</script>
<style scoped>
.body{
            user-select: none;
        }
audio {
  display: block;
  margin-bottom: 10px;
}
#audio-container {
  padding: 20px 0;
}
.ui-btn {
  display: inline-block;
  padding: 5px 20px;
  font-size: 14px;
  line-height: 1.428571429;
  box-sizing: content-box;
  text-align: center;
  border: 1px solid #e8e8e8;
  border-radius: 3px;
  color: #555;
  background-color: #fff;
  border-color: #e8e8e8;
  white-space: nowrap;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.ui-btn:hover,
.ui-btn.hover {
  color: #333;
  text-decoration: none;
  background-color: #f8f8f8;
  border: 1px solid #ddd;
}
.ui-btn:focus,
.ui-btn:active {
  color: #333;
  outline: 0;
}
.ui-btn.disabled,
.ui-btn.disabled:hover,
.ui-btn.disabled:active,
.ui-btn[disabled],
.ui-btn[disabled]:hover,
.ui-state-disabled .ui-btn {
  cursor: not-allowed;
  background-color: #eee;
  border-color: #eee;
  color: #aaa;
}
.ui-btn-primary {
  color: #fff;
  background-color: #39b54a;
  border-color: #39b54a;
  position: fixed;
  bottom: 1.5rem;
  width: 80%;
  margin-left: 10%;
  padding: 0.5rem 0;
}
.ui-btn-primary:hover,
.ui-btn-primary.hover {
  color: #fff;
  background-color: #16a329;
  border-color: #16a329;
}
.ui-btn-primary:focus,
.ui-btn-primary:active {
  color: #fff;
}
.ui-btn-primary.disabled:focus {
  color: #aaa;
}
img {
  display: block;
  width: 40%;
  margin: auto;
}
body {
  margin: 0;
  padding: 0;
}
#mask {
  width: 43%;
  background: rgba(0, 0, 0, 0.05);
  padding: 3rem 0 1rem 0;
  display: none;
  margin: 2rem auto;
  margin-top: 51%;
}
#mask p {
  text-align: center;
  font-size: 0.8rem;
  color: rgba(0, 0, 0, 0.5);
}
</style>
