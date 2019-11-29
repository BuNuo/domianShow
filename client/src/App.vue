<template>
  <div id="app">
    <Row>
      <Col span="6">
      <div class="main-wrapper" style="position: relative; top: -6vh;">
        <div class="container main-sentence justify-content-center text-center">
          <span ref="dujitang" style="font-size: 2rem;"></span>
        </div>
      </div>
      <div class="foot-1" style="position: absolute; bottom: 7vh;width: 100%;">
        <div class="container">
          <div class="row">
            <div class="col text-center">
              <button class="btn btn-primary btn-filled btn-xs" @click="randomSentence()">再来一碗</button>
            </div>
          </div>
        </div>
      </div>
      </Col>
      <Col span="12">
      <div class="body-content">
        <div class="demo">
          <div class="demo-top">
            <div class="demo-domain">hackcrown.com</div>
            <div class="demo-h4">您正在访问的域名 <span class="domain">hackcrown.com</span> 可以转让!如果您对该域名感兴趣，请<a href="javascript:void(0)" target="_blank">点击这里</a>购买。</div>
            <div class="demo-h4">This domain name <span class="domain">hackcrown.com</span> is for sale! If you would like to purchase this domain name, please <a href="javascript:void(0)" target="_blank">click here</a>to buy。</div>
            <div class="btn-center"></div>
          </div>
          <div class="main-box clearfix">
            <div class="sale-box FL-L">
              <div class="box-title">域名简介</div>
              <div class="box-text">
                1、hackcrown.com
              </div>
              <div class="box-text">2、通过联系域名经纪人帮您联系购买域名</div>
              <div class="box-text">3、通过致电我们：4006602522</div>
              <br>
            </div>
            <div class="contact-box FL-R">
              <div class="box-title">联系方式</div>
              <dl>
                <dt>邮箱：</dt>
                <dd>hackcrown@163.com</dd>
                <dt>电话：</dt>
                <dd>13717740306</dd>
                <dt>Q Q：</dt>
                <dd>1434244213</dd>
              </dl>
            </div>
          </div>
        </div>
      </div>
      </Col>
      <Col span="6">
      <div class="main-wrapper" style="position: relative; top: -6vh;">
        <div class="container main-sentence justify-content-center text-center">
          <span ref="duanzi" style="font-size: 2rem;"></span>
        </div>
      </div>
      <div class="foot-1" style="position: absolute; bottom: 7vh;width: 100%;">
        <div class="container">
          <div class="row">
            <div class="col text-center">
              <button class="btn btn-primary btn-filled btn-xs" @click="duanzi()">再来一击</button>
            </div>
          </div>
        </div>
      </div>
      </Col>
    </Row>
  </div>
</template>
<script>
import './assets/static/css/app.css'
import './assets/static/css/demo9.css'
import dujitang from './assets/static/js/index.js'
import getDuanzi from './assets/static/js/duanzi'
export default {
  name: 'app',
  data() {
    return {

    }

  },
  created() {


  },
  mounted() {
    this.randomSentence()
    this.duanzi()
  },
  methods: {
    randomSentence: function() {
      this.$refs.dujitang.innerText = dujitang.randomSentence()
    },
    duanzi: function() {
      this.$refs.duanzi.innerHTML = getDuanzi()
    }
  }
}

</script>
<style>
