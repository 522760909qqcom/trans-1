# trans-1
transfrom
*{
	margin: 0 auto;
	padding: 0;
}
html{
	height: 100%;
	background: linear-gradient(#29f9f0 0%,#000 80%) no-repeat;
}
div.wrap{
	height: 200px;
	width: 200px;
	perspective: 1000px;
	margin-top: 200px;
}
.cube{
	width: 200px;
	height: 200px;
	position: relative;
	color: #ff92ff;
	font-size: 36px;
	font-weight: 100;
	text-align: center;
	line-height: 200px;
	transform-style: preserve-3d;
	transform: rotateX(-17deg) rotateY(-0deg) rotateZ(2deg);
	animation: move 24s ;infinite linear;
}
.cube:hover{
	cursor: pointer;

}
@keyframes move{
	0%{
		transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg);
	}
	100%{
		transform: rotateX(720deg) rotateY(720deg) rotateZ(720deg);
	}

}
.cube>div{
	position: absolute;
	width: 100%;
	height: 100%;
	border: 10px solid #66daff;
	border-radius: 20px;
	background-color: rgba(51,51,51,.3);
}
.cube:hover>div.out-back{
	transform: translateZ(-200px) rotateY(180deg);
}
.cube:hover>div.out-front{
	transform: translateZ(200px);
}
.cube:hover>div.out-left{
	transform: translateX(-200px) rotateY(-90deg);
}
.cube:hover>div.out-right{
	transform: translateX(200px) rotateY(90deg);
}
.cube:hover>div.out-top{
	transform: translateY(-200px) rotateX(90deg);
}
.cube:hover>div.out-bottom{
	transform: translateY(200px) rotateX(-90deg);
}
.cube>div.out-back{
	transform: translateZ(-100px) rotateY(180deg);
}
.cube>div.out-front{
	transform: translateZ(100px);
}
.cube>div.out-left{
	transform: translateX(-100px) rotateY(-90deg);
}
.cube>div.out-right{
	transform: translateX(100px) rotateY(90deg);
}
.cube>div.out-top{
	transform: translateY(-100px) rotateX(90deg);
}
.cube>div.out-bottom{
	transform: translateY(100px) rotateX(-90deg);
}
.cube>div.in{
	position: relative;
	width: 80px;
	height: 80px;
	background-color: inherit;
	/*border: 3px solid #ffe7f9;*/
	font-weight: bold;
	font-size: 30px;
	color: #fff;
	border: none;
}
.cube>div.in>div{
	position: absolute;
	background-color: rgba(20,20,20,0.5);
	border-radius: 20px;
	border: 3px solid #ffe7f9;
	text-align: center;
	line-height: 80px;
	width: 80px;
	height: 80px;
	top: 50%;
	left: 50%;
	margin-left: -40px;
	margin-top: 30px;
}
.cube>div.in>div.in-front{
	transform: translateZ(40px);
}
.cube>div.in>div.in-back{
	transform: translateZ(-40px) rotateY(180deg);
}
.cube>div.in>div.in-left{
	transform: translateX(-40px) rotateY(-90deg);
}
.cube>div.in>div.in-right{
	transform: translateX(40px) rotateY(90deg);
}
.cube>div.in>div.in-top{
	transform: translateY(-40px) rotateX(-90deg);
}
.cube>div.in>div.in-bottom{
	transform: translateY(40px) rotateX(90deg);
}

<html lang="en">
<head>
	<title>transfrom</title>
	<meta charest="utf-8">
	<link rel="stylesheet" type="text/css" href="transfrom.css">
</head>
<body>
<div class="wrap">
	<div class="cube">
		<div class="out-front">前面</div>
		<div class="out-back">后面</div>
		<div class="out-left">左面</div>
		<div class="out-right">右面</div>
		<div class="out-top">上面</div>
		<div class="out-bottom">下面</div>
		<div class="in">
			<div class="in-front">1</div>
			<div class="in-back">2</div>
			<div class="in-left">3</div>
			<div class="in-right">4</div>
			<div class="in-top">5</div>
			<div class="in-bottom">6</div>
		</div>
		
	</div>
</div>
</body>
</html>
