# lol
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="style.css">
<style>
div{margin:50px auto}
div div div{font-size:30px}
div div div img{width:100%;height:100%}

.wrap {
        perspective: 800px;
        perspective-origin: 50% 100px;
}

.cube {
        position: relative;
        width: 200px;
        transform-style: preserve-3d;
}

.cube div {
        position: absolute;
        width: 200px;
        height: 200px;
}

.back {
        transform: translateZ(-100px) rotateY(180deg);
}
.right {
        transform: rotateY(-270deg) translateX(100px);
        transform-origin: top right;
}
.left {
        transform: rotateY(270deg) translateX(-100px);
        transform-origin: center left;
}
.top {
        transform: rotateX(-90deg) translateY(-100px);
        transform-origin: top center;
}
.bottom {
        transform: rotateX(90deg) translateY(100px);
        transform-origin: bottom center;
}
.front {
        transform: translateZ(100px);
}

@keyframes spin {
        from { transform: rotateY(0); }
        to { transform: rotateY(360deg); }
}

.cube {
        animation: spin 5s infinite linear;
}

@keyframes spin-vertical {
        from { transform: rotateX(0); }
        to { transform: rotateX(-360deg); }
}

.cube-wrap.vertical .cube {
        margin: 0 auto; /* keeps the cube centered */

        transform-origin: 0 100px;
        animation: spin-vertical 5s infinite linear;
}

.cube-wrap.vertical .top {
        transform: rotateX(-270deg) translateY(-100px);
}

.cube-wrap.vertical .back {
        transform: translateZ(-100px) rotateX(180deg);
}

.cube-wrap.vertical .bottom {
        transform: rotateX(-90deg) translateY(100px);
}
	</style>
</head>	
<body>
<div class="wrap">
	<div class="cube">
		<div class="front"><img src="./lolface.png"/></div>
		<div class="back"><img src="./lolface.png"/></div>
		<div class="top"><img src="./lolface.png"/></div>
		<div class="bottom"><img src="./lolface.png"/></div>
		<div class="left"><img src="./lolface.png"/></div>
		<div class="right"><img src="./lolface.png"/></div>
	</div>
</div>
</body>
</html>
