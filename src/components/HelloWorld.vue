<template>
  <div class="hello">
    <h3>{{name}}</h3>
    <div class="hint-wrap">
      <div class="hint-text">
        有效期还有<span class="hint-number">{{day}}</span>天
      </div>
      <div class="hint-split"></div>
      <div class="renew-btn">申请更新</div>
    </div>
    <div>
      <div class="qrcode">
        <canvas width="180" height="180" id="qrcode" />
      </div>
    </div>
    <div>
      <div class="vcode-wrap">
        <div>验证码</div>
        <div class="vcode">{{vcode}}</div>
      </div>
    </div>
    <div class="mng-link">
      <div>穗康码管理</div>
      <img
        width="12"
        height="12"
        style="margin: 0 8px; display: inline-block"
        src="@/assets/next.svg"
      />
    </div>
    <div class="option-box">
      <div class="option-title">最新健康自报</div>
      <div>
        <img src="@/assets/dummy.png" width="100%" alt />
      </div>
      <div class="option-title">个人关联信息</div>
    </div>
  </div>
</template>

<script>
import QRCode from "qrcode";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: () => {
    return {
      name: "李*所",
      day: 1,
      vcode: "1919 8100"
    };
  },
  mounted() {
    var canvas = document.getElementById("qrcode");
    QRCode.toCanvas(canvas, "dshaufhdiusahcvhdsadsafdsaflkdsklafhkldsahklf", {
      errorCorrectionLevel: 'H'
    },function(error) {
      console.log(error);
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  padding-top: 40px;
  color: white;
}

h3 {
  margin-bottom: 6px;
}

.hint-wrap {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 10px;
}

.hint-split {
  margin: 0 10pt 0 10pt;
  height: 12pt;
  width: 1pt;
  background-color: lightgray;
}

.hint-number {
  font-size: normal;
  font-weight: bold;
  margin: 0px 8px;
}

.hint-text {
  font-weight: lighter;
  font-size: 15px;
}

.renew-btn {
  display: inline-block;
  padding: 2pt 8pt 2pt 8pt;
  border-radius: 10pt;
  border: 1px solid white;
  font-size: 8pt;
  background-color: #fafafa22;
}

.qrcode {
  width: 200px;
  height: 200px;
  border-radius: 5pt;
  background-color: white;
  border: 1px solid #0f0f0f22;
  margin: 0 auto;
}

.vcode-wrap {
  margin-top: 10pt;
  font-size: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.vcode {
  margin: 0 8px;
  padding: 1px 6px;
  border-radius: 3pt;
  font-size: 15px;
  background-color: #ffffff33;
  font-weight: bold;
}

.mng-link {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 50px 0 25px 0;
  font-weight: lighter;
  font-size: 14px;
}

.option-box {
  height: 300px;
  background-color: white;
  color: black;
  text-align: left;
}

.option-title {
  font-size: 16pt;
  padding: 18pt;
  font-weight: bold;
}
</style>
