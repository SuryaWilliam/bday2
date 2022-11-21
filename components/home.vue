<template>
  <div class="bg-black">
    <div
      class="relative flex items-center justify-center h-screen overflow-hidden"
    >
      <template>
        <video
          autoplay
          loop
          muted
          playsinline
          class="fixed w-full hidden min-[500px]:flex"
          id="bgc"
        >
          <source src="/bgc.mp4" type="video/mp4" />
        </video>
        <video
          autoplay
          loop
          muted
          playsinline
          class="fixed w-full min-[500px]:hidden"
          id="bgcm"
        >
          <source src="/bgcm.mp4" type="video/mp4" />
        </video>
      </template>
      <template>
        <video
          autoplay
          loop
          muted
          playsinline
          class="fixed w-full max-w-[500px]:hidden"
          id="bg"
        >
          <source src="/bg.mp4" type="video/mp4" />
        </video>
        <video
          autoplay
          loop
          muted
          playsinline
          class="fixed w-full min-[500px]:hidden"
          id="bgm"
        >
          <source src="/bgm.mp4" type="video/mp4" />
        </video>
      </template>
    </div>
    <div
      id="myb"
      class="fixed flex justify-center items-center text-[#ffffc6] text-4xl lg:text-8xl z-50 left-1/2 top-1/2 lg:top-[510px] -translate-x-1/2 -translate-y-1/2"
    ></div>
    <div class="" id="test"></div>
  </div>
</template>

<script>
export default {
  name: "home",
};

var countDownDate = new Date("Nov 27, 2022 18:00:00").getTime();

var ameibday = setInterval(function () {
  var now = new Date().getTime();

  var distance = countDownDate - now;

  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  document.getElementById("myb").innerHTML =
    "<div class='flex justify-center items-center'><div class='mx-2 lg:mx-5 text-center lg:w-[120px]'><div>" +
    days +
    "</div><div class='text-base lg:text-4xl'>Hari</div></div><div class='mx-2 lg:mx-5 text-center lg:w-[120px]'><div>" +
    hours +
    "</div><div class='text-base lg:text-4xl'>Jam</div></div><div class='mx-2 lg:mx-5 text-center lg:w-[120px]'><div>" +
    minutes +
    "</div><div class='text-base lg:text-4xl'>Menit</div></div><div class='mx-2 lg:mx-5 text-center lg:w-[120px]'><div>" +
    seconds +
    "</div><div class='text-base lg:text-4xl'>Detik</div></div></div>";

  if (distance < 0) {
    clearInterval(ameibday);
    document.getElementById("myb").innerHTML = "";

    document.getElementById("test").innerHTML =
      "<div class='cake z-50 min-[500px]:hidden'><div class='plate'></div><div class='layer layer-bottom'></div><div class='layer layer-middle'></div><div class='layer layer-top'></div><div class='icing'></div><div class='drip drip1'></div><div class='drip drip2'></div><div class='drip drip3'></div><div class='candle'><div class='flame'></div></div></div>";
    document.getElementById("bg").style.display = "none";
    document.getElementById("bgm").style.display = "none";
  }
}, 1000);
</script>

<style>
#myb {
  text-shadow: 0 0 1px rgba(255, 210, 108, 1), 0 0 5px rgba(255, 210, 108, 1),
    0 0 10px rgba(255, 210, 108, 1), 0 0 15px rgba(0, 0, 0, 1),
    0 0 20px rgba(0, 0, 0, 1);
  font-weight: bold;
}

.cake {
  position: absolute;
  width: 125px;
  height: 200px;
  top: 65%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.plate {
  width: 145px;
  height: 45px;
  position: absolute;
  bottom: 55px;
  left: -10px;
  background-color: #ccc;
  border-radius: 50%;
  box-shadow: 0 2px 0 #b3b3b3, 0 4px 0 #b3b3b3, 0 5px 40px rgba(0, 0, 0, 0.5);
}

.cake > * {
  position: absolute;
}

.layer {
  position: absolute;
  display: block;
  width: 125px;
  height: 45px;
  border-radius: 50%;
  background-color: #553c13;
  box-shadow: 0 2px 0px #6a4b18, 0 4px 0px #33240b, 0 6px 0px #32230b,
    0 8px 0px #31230b, 0 10px 0px #30220b, 0 12px 0px #2f220b,
    0 14px 0px #2f210a, 0 16px 0px #2e200a, 0 18px 0px #2d200a,
    0 20px 0px #2c1f0a, 0 22px 0px #2b1f0a, 0 24px 0px #2a1e09,
    0 26px 0px #2a1d09, 0 28px 0px #291d09, 0 30px 0px #281c09;
}

.layer-top {
  top: 0px;
}

.layer-middle {
  top: 33px;
}

.layer-bottom {
  top: 66px;
}

.icing {
  top: 0px;
  left: 1px;
  background-color: #f0e4d0;
  width: 122px;
  height: 45px;
  border-radius: 50%;
}
.icing:before {
  content: "";
  position: absolute;
  top: 4px;
  right: 5px;
  bottom: 6px;
  left: 5px;
  background-color: #f4ebdc;
  box-shadow: 0 0 4px #f6efe3, 0 0 4px #f6efe3, 0 0 4px #f6efe3;
  border-radius: 50%;
  z-index: 1;
}

.drip {
  display: block;
  width: 50px;
  height: 60px;
  border-bottom-left-radius: 25px;
  border-bottom-right-radius: 25px;
  background-color: #f0e4d0;
}

.drip1 {
  top: 25px;
  left: 5px;
  transform: skewY(15deg);
  height: 24px;
  width: 20px;
}

.drip2 {
  top: 25px;
  left: 90px;
  height: 30px;
  width: 30px;
  transform: skewY(-15deg);
}

.drip3 {
  top: 35px;
  left: 30px;
  width: 55px;
  height: 35px;
  border-bottom-left-radius: 40px;
  border-bottom-right-radius: 40px;
}

.candle {
  background-color: #7b020b;
  width: 12px;
  height: 40px;
  border-radius: 8px/4px;
  top: -15px;
  left: 50%;
  margin-left: -5px;
  z-index: 10;
}
.candle:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 12px;
  height: 8px;
  border-radius: 50%;
  background-color: #ad030f;
}

.flame {
  position: absolute;
  background-color: #ffa500;
  width: 10px;
  height: 25px;
  border-radius: 10px 10px 10px 10px/25px 25px 10px 10px;
  top: -25px;
  left: 50%;
  margin-left: -5px;
  z-index: 10;
  box-shadow: 0 0 10px rgba(255, 165, 0, 0.5), 0 0 20px rgba(255, 165, 0, 0.5),
    0 0 60px rgba(255, 165, 0, 0.5), 0 0 80px rgba(255, 165, 0, 0.5);
  transform-origin: 50% 90%;
  animation: flicker 1s ease-in-out alternate infinite;
}

@keyframes flicker {
  0% {
    transform: skewX(5deg);
    box-shadow: 0 0 10px rgba(255, 165, 0, 0.2), 0 0 20px rgba(255, 165, 0, 0.2),
      0 0 60px rgba(255, 165, 0, 0.2), 0 0 80px rgba(255, 165, 0, 0.2);
  }
  25% {
    transform: skewX(-5deg);
    box-shadow: 0 0 10px rgba(255, 165, 0, 0.5), 0 0 20px rgba(255, 165, 0, 0.5),
      0 0 60px rgba(255, 165, 0, 0.5), 0 0 80px rgba(255, 165, 0, 0.5);
  }
  50% {
    transform: skewX(10deg);
    box-shadow: 0 0 10px rgba(255, 165, 0, 0.3), 0 0 20px rgba(255, 165, 0, 0.3),
      0 0 60px rgba(255, 165, 0, 0.3), 0 0 80px rgba(255, 165, 0, 0.3);
  }
  75% {
    transform: skewX(-10deg);
    box-shadow: 0 0 10px rgba(255, 165, 0, 0.4), 0 0 20px rgba(255, 165, 0, 0.4),
      0 0 60px rgba(255, 165, 0, 0.4), 0 0 80px rgba(255, 165, 0, 0.4);
  }
  100% {
    transform: skewX(5deg);
    box-shadow: 0 0 10px rgba(255, 165, 0, 0.5), 0 0 20px rgba(255, 165, 0, 0.5),
      0 0 60px rgba(255, 165, 0, 0.5), 0 0 80px rgba(255, 165, 0, 0.5);
  }
}
</style>
