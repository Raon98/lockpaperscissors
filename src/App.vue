<template>
  <div>
    <div id="computer" :style="computeStyleObject"></div>
    <div>
      <button :style="{background: coaa}" @onClick="onClickButton()">바위</button>
      <button @onClick="onClickButton('가위')">가위</button>
      <button @onClick="onClickButton('보')">보</button>
    </div>
    <div>{{result}}</div>
    <div>현재 {{score}}점</div>
  </div>
</template>

<script>
const rspCoords = {
  바위 : '0',
  가위 : "-142px",
  보 : "-284px",
}

export default {
  data(){
    return{
      coaa : '',
      imgCoord: rspCoords.바위,
      result: '',
      score: 0,
    }
  },
  computed: {
    computeStyleObject() {
      return{
        background: `url(http://en.pimg.jp/023/182/267/1/23182267.jpg) ${this.imgCoord} 0`,
      };
    },
  },
  methods: {
    // eslint-disable-next-line no-unused-vars
    onClickButton() {
      this.coaa = 'red'
    },
    onclick: function (){
      this.coaa = 'red'
    }
  },

};
</script>

<style>
#computer {
  width: 142px;
  height: 200px;
  background-position: 0 0;
}
</style>
