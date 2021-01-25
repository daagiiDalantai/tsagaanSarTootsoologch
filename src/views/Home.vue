<template>
  <div class="home" id="wm-visualdata">
    <div class="center-body">
      <input type="text" @change="changeYear" v-model="year" minlength="0" maxlength="8"  clear/>
      <div>
        <el-row>
          <el-col :span="24"><div class="grid-content bg-purple-dark">
             <el-image
                style="width: 150px; height: 150px"
                :src="nowImage"
                fit="cover"></el-image>
            </div></el-col>
        </el-row>
          <el-row>
          <el-col :span="24"><div class="grid-content bg-purple-dark">
            <span class="text-style">Жил: {{res.Жил}}</span><br/>
            <span class="text-style">Жаран: {{res.Жаран}}</span><br/>
            <span class="text-style">Жилийн мэнгэ: {{res.Жилийн_мэнгэ}}</span><br/>
            <span class="text-style">Шинийн нэгэн: {{res.Шинийн_нэгэн}}</span><br/>
            <span class="text-style">Өдрийн өнгө: {{res.Өдрийн_өнгө}}</span><br/>
            <span class="text-style">Өдрийн мэнгэ: {{res.Өдрийн_мэнгэ}}</span><br/>
            <span class="text-style">Суудал: {{res.Суудал}}</span><br/>
            <span class="text-style">Битүүний сар: {{res.Битүүний_сар}}</span><br/>
            </div></el-col>
        </el-row>
      </div>
    </div>
  </div>
</template>

<script>
import calculateNewYear from '../helper'

export default {
  name: 'Home',
  components: {},
  data () {
    return {
      year: 2021,
      res: {},
      nowImage: '',
      mouseImg: 'https://content.ikon.mn/ikon/dv/mur/1.png',
      cowImg: 'https://content.ikon.mn/ikon/dv/mur/2.png',
      tigerImg: 'https://content.ikon.mn/ikon/dv/mur/3.png',
      rabbitImg: 'https://content.ikon.mn/ikon/dv/mur/4.png',
      dragonImg: 'https://content.ikon.mn/ikon/dv/mur/5.png',
      snakeImg: 'https://content.ikon.mn/ikon/dv/mur/6.png',
      horseImg: 'https://content.ikon.mn/ikon/dv/mur/7.png',
      sheepImg: 'https://content.ikon.mn/ikon/dv/mur/8.png',
      monkeyImg: 'https://content.ikon.mn/ikon/dv/mur/9.png',
      chickenImg: 'https://content.ikon.mn/ikon/dv/mur/10.png',
      dogImg: 'https://content.ikon.mn/ikon/dv/mur/11.png',
      pigImg: 'https://content.ikon.mn/ikon/dv/mur/12.png'
    }
  },
  created () {
    this.res = calculateNewYear(this.year)
    var salgasanJil = this.res.Жил.split(' ')
    if (salgasanJil[1] === 'хулгана') {
      this.nowImage = this.mouseImg
    } else if (salgasanJil[1] === 'үхэр') {
      this.nowImage = this.cowImg
    } else if (salgasanJil[1] === 'бар') {
      this.nowImage = this.tigerImg
    } else if (salgasanJil[1] === 'туулай') {
      this.nowImage = this.rabbitImg
    } else if (salgasanJil[1] === 'луу') {
      this.nowImage = this.dragonImg
    } else if (salgasanJil[1] === 'могой') {
      this.nowImage = this.snakeImg
    } else if (salgasanJil[1] === 'морь') {
      this.nowImage = this.horseImg
    } else if (salgasanJil[1] === 'хонь') {
      this.nowImage = this.sheepImg
    } else if (salgasanJil[1] === 'бич') {
      this.nowImage = this.monkeyImg
    } else if (salgasanJil[1] === 'тахиа') {
      this.nowImage = this.chickenImg
    } else if (salgasanJil[1] === 'нохой') {
      this.nowImage = this.dogImg
    } else if (salgasanJil[1] === 'гахай') {
      this.nowImage = this.pigImg
    }
  },
  methods: {
    changeYear () {
      this.res = calculateNewYear(this.year)
      var salgasanJil = this.res.Жил.split(' ')
      if (salgasanJil[1] === 'хулгана') {
        this.nowImage = this.mouseImg
      } else if (salgasanJil[1] === 'үхэр') {
        this.nowImage = this.cowImg
      } else if (salgasanJil[1] === 'бар') {
        this.nowImage = this.tigerImg
      } else if (salgasanJil[1] === 'туулай') {
        this.nowImage = this.rabbitImg
      } else if (salgasanJil[1] === 'луу') {
        this.nowImage = this.dragonImg
      } else if (salgasanJil[1] === 'могой') {
        this.nowImage = this.snakeImg
      } else if (salgasanJil[1] === 'морь') {
        this.nowImage = this.horseImg
      } else if (salgasanJil[1] === 'хонь') {
        this.nowImage = this.sheepImg
      } else if (salgasanJil[1] === 'бич') {
        this.nowImage = this.monkeyImg
      } else if (salgasanJil[1] === 'тахиа') {
        this.nowImage = this.chickenImg
      } else if (salgasanJil[1] === 'нохой') {
        this.nowImage = this.dogImg
      } else if (salgasanJil[1] === 'гахай') {
        this.nowImage = this.pigImg
      }
    }
  }
}
</script>
<style scoped>
#wm-visualdata {
  background: url("https://content.ikon.mn/raw/2020/2/17/10661/xas2.png") repeat;
  position: relative;
  clear: both;
  height: 800px;
}
</style>
