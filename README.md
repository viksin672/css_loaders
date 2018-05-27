# css_loaders
<h1>css loader using keyframes..</h1>
<h2>Style.css</h2>
<p>html, body{
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  font-family: 'Open Sans', sans-serif;
}

a{
  text-decoration: none;
}

/* GRID */

.twelve { width: 100%; }
.eleven { width: 91.53%; }
.ten { width: 83.06%; }
.nine { width: 74.6%; }
.eight { width: 66.13%; }
.seven { width: 57.66%; }
.six { width: 49.2%; }
.five { width: 40.73%; }
.four { width: 32.26%; }
.three { width: 23.8%; }
.two { width: 15.33%; }
.one { width: 6.866%; }

/* COLUMNS */

.col {
	display: block;
	float:left;
	margin: 1% 0 1% 1.6%;
}

.col:first-of-type {
  margin-left: 0;
}

.container{
  width: 100%;
  max-width: 940px;
  margin: 0 auto;
  position: relative;
  text-align: center;
}

/* CLEARFIX */

.cf:before,
.cf:after {
    content: " ";
    display: table;
}

.cf:after {
    clear: both;
}

.cf {
    *zoom: 1;
}

.row{
  margin: 30px 0;
}

.three{
  background-color: #eee;
  padding: 50px 0;
}

/* ALL LOADERS */

.loader{
  width: 100px;
  height: 100px;
  border-radius: 100%;
  position: relative;
  margin: 0 auto;
}

/* LOADER 1 */

#loader-1:before, #loader-1:after{
  content: "";
  position: absolute;
  top: -10px;
  left: -10px;
  width: 100%;
  height: 100%;
  border-radius: 100%;
  border: 10px solid transparent;
  border-top-color: #3498db;
}

#loader-1:before{
  z-index: 100;
  animation: spin 1s infinite;
}

#loader-1:after{
  border: 10px solid #ccc;
}

@keyframes spin{
  0%{
    -webkit-transform: rotate(0deg);
    -ms-transform: rotate(0deg);
    -o-transform: rotate(0deg);
    transform: rotate(0deg);
  }

  100%{
    -webkit-transform: rotate(360deg);
    -ms-transform: rotate(360deg);
    -o-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}

/* LOADER 2 */

#loader-2 span{
  display: inline-block;
  width: 20px;
  height: 20px;
  border-radius: 100%;
  background-color: #3498db;
  margin: 35px 5px;
}

#loader-2 span:nth-child(1){
  animation: bounce 1s ease-in-out infinite;
}

#loader-2 span:nth-child(2){
  animation: bounce 1s ease-in-out 0.33s infinite;
}

#loader-2 span:nth-child(3){
  animation: bounce 1s ease-in-out 0.66s infinite;
}

@keyframes bounce{
  0%, 75%, 100%{
    -webkit-transform: translateY(0);
    -ms-transform: translateY(0);
    -o-transform: translateY(0);
    transform: translateY(0);
  }

  25%{
    -webkit-transform: translateY(-20px);
    -ms-transform: translateY(-20px);
    -o-transform: translateY(-20px);
    transform: translateY(-20px);
  }
}

/* LOADER 3 */

#loader-3:before, #loader-3:after{
  content: "";
  width: 20px;
  height: 20px;
  position: absolute;
  top: 0;
  left: calc(50% - 10px);
  background-color: #3498db;
  animation: squaremove 1s ease-in-out infinite;
}

#loader-3:after{
  bottom: 0;
  animation-delay: 0.5s;
}

@keyframes squaremove{
  0%, 100%{
    -webkit-transform: translate(0,0) rotate(0);
    -ms-transform: translate(0,0) rotate(0);
    -o-transform: translate(0,0) rotate(0);
    transform: translate(0,0) rotate(0);
  }

  25%{
    -webkit-transform: translate(40px,40px) rotate(45deg);
    -ms-transform: translate(40px,40px) rotate(45deg);
    -o-transform: translate(40px,40px) rotate(45deg);
    transform: translate(40px,40px) rotate(45deg);
  }

  50%{
    -webkit-transform: translate(0px,80px) rotate(0deg);
    -ms-transform: translate(0px,80px) rotate(0deg);
    -o-transform: translate(0px,80px) rotate(0deg);
    transform: translate(0px,80px) rotate(0deg);
  }

  75%{
    -webkit-transform: translate(-40px,40px) rotate(45deg);
    -ms-transform: translate(-40px,40px) rotate(45deg);
    -o-transform: translate(-40px,40px) rotate(45deg);
    transform: translate(-40px,40px) rotate(45deg);
  }
}

/* LOADER 4 */

#loader-4 span{
  display: inline-block;
  width: 20px;
  height: 20px;
  border-radius: 100%;
  background-color: #3498db;
  margin: 35px 5px;
  opacity: 0;
}

#loader-4 span:nth-child(1){
  animation: opacitychange 1s ease-in-out infinite;
}

#loader-4 span:nth-child(2){
  animation: opacitychange 1s ease-in-out 0.33s infinite;
}

#loader-4 span:nth-child(3){
  animation: opacitychange 1s ease-in-out 0.66s infinite;
}

@keyframes opacitychange{
  0%, 100%{
    opacity: 0;
  }

  60%{
    opacity: 1;
  }
}

/* LOADER 5 */

#loader-5 span{
  display: block;
  position: absolute;
  left: calc(50% - 20px);
  top: calc(50% - 20px);
  width: 20px;
  height: 20px;
  background-color: #3498db;
}

#loader-5 span:nth-child(2){
  animation: moveanimation1 1s ease-in-out infinite;
}

#loader-5 span:nth-child(3){
  animation: moveanimation2 1s ease-in-out infinite;
}

#loader-5 span:nth-child(4){
  animation: moveanimation3 1s ease-in-out infinite;
}

@keyframes moveanimation1{
  0%, 100%{
    -webkit-transform: translateX(0px);
    -ms-transform: translateX(0px);
    -o-transform: translateX(0px);
    transform: translateX(0px);
  }

  75%{
    -webkit-transform: translateX(30px);
    -ms-transform: translateX(30px);
    -o-transform: translateX(30px);
    transform: translateX(30px);
  }
}

@keyframes moveanimation2{
  0%, 100%{
    -webkit-transform: translateY(0px);
    -ms-transform: translateY(0px);
    -o-transform: translateY(0px);
    transform: translateY(0px);
  }

  75%{
    -webkit-transform: translateY(30px);
    -ms-transform: translateY(30px);
    -o-transform: translateY(30px);
    transform: translateY(30px);
  }
}

@keyframes moveanimation3{
  0%, 100%{
    -webkit-transform: translate(0px, 0px);
    -ms-transform: translate(0px, 0px);
    -o-transform: translate(0px, 0px);
    transform: translate(0px, 0px);
  }

  75%{
    -webkit-transform: translate(30px, 30px);
    -ms-transform: translate(30px, 30px);
    -o-transform: translate(30px, 30px);
    transform: translate(30px, 30px);
  }
}

/* LOADER 6 */

#loader-6{
  top: 40px;
  left: -2.5px;
}

#loader-6 span{
  display: inline-block;
  width: 5px;
  height: 20px;
  background-color: #3498db;
}

#loader-6 span:nth-child(1){
  animation: grow 1s ease-in-out infinite;
}

#loader-6 span:nth-child(2){
  animation: grow 1s ease-in-out 0.15s infinite;
}

#loader-6 span:nth-child(3){
  animation: grow 1s ease-in-out 0.30s infinite;
}

#loader-6 span:nth-child(4){
  animation: grow 1s ease-in-out 0.45s infinite;
}

@keyframes grow{
  0%, 100%{
    -webkit-transform: scaleY(1);
    -ms-transform: scaleY(1);
    -o-transform: scaleY(1);
    transform: scaleY(1);
  }

  50%{
    -webkit-transform: scaleY(1.8);
    -ms-transform: scaleY(1.8);
    -o-transform: scaleY(1.8);
    transform: scaleY(1.8);
  }
}

/* LOADER 7 */

#loader-7{
  -webkit-perspective: 120px;
  -moz-perspective: 120px;
  -ms-perspective: 120px;
  perspective: 120px;
}

#loader-7:before{
  content: "";
  position: absolute;
  left: 25px;
  top: 25px;
  width: 50px;
  height: 50px;
  background-color: #3498db;
  animation: flip 1s infinite;
}

@keyframes flip {
  0% {
    transform: rotate(0);
  }

  50% {
    transform: rotateY(180deg);
  }

  100% {
    transform: rotateY(180deg)  rotateX(180deg);
  }
}

/* LOADER 8 */

#loader-8:before{
  content: "";
  position: absolute;
  width: 10px;
  height: 10px;
  top: calc(50% - 10px);
  left: 0px;
  background-color: #3498db;
  animation: rotatemove 1s infinite;
}

@keyframes rotatemove{
  0%{
    -webkit-transform: scale(1) translateX(0px);
    -ms-transform: scale(1) translateX(0px);
    -o-transform: scale(1) translateX(0px);
    transform: scale(1) translateX(0px);
  }

  100%{
    -webkit-transform: scale(2) translateX(45px);
    -ms-transform: scale(2) translateX(45px);
    -o-transform: scale(2) translateX(45px);
    transform: scale(2) translateX(45px);
  }
}</p>
