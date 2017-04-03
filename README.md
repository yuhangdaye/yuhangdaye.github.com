
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style type="text/css">
		body{
			background: #000;
			
		}
		*{
			margin: 0;
			padding:0;
			list-style: none;
		}
		ul{
			width: 300px;
			height: 300px;
			position: absolute;
			left: 50%;
			top: 35%;
			margin: -150px 0 0 -150px;
			perspective: 800px;


		}
		ul li{
			 width:100%;
            height:100%;
            position: absolute;
            left:0;
            top:0;
            background: #399;
            border: 1px solid #fff;
            font-size: 50px;
            text-align: center;
            line-height: 300px;
            color: #fff;
            text-shadow: 2px 2px 5px #000;
            opacity: 0;
            transition: 1s all ease;
            -webkit-box-reflect:below 20px -webkit-linear-gradient(rgba(0,0,0,0) 40%, rgba(0,0,0,.8));
            
		}
		.left{
			transform:translateX(-200px) rotateY(60deg);
			opacity: 0.7;
			z-index: 2
		}
		.first{
			transform:translateX(-280px) rotateY(60deg);
			opacity: 0;
		}
		.conter{
			transform:translateZ(0px);
			opacity: 1;
			z-index: 3
		}
		.right{
			transform: translateX(200px) rotateY(-60deg);
			opacity: 0.7;
			z-index: 2;
		}
		.last{
			transform: translateX(280px) rotateY(-60deg);
			opacity: 0;
			z-index: 1;
		}
		input{
			margin-top: 20px;
			margin-right: 20px;
			width: 40px;
			height: 30px;
			

		}
		li img{
			width: 100%;
			height: 100%
		}
		div{width: 100%; text-align: center;}
	</style>
	<script type="text/javascript">
		window.onload=function(){
			var Btn1=document.querySelector('.val1')
			var Btn2=document.querySelector('.val2')
			var aLi=document.querySelectorAll('li')
			var aClass=[];
			for (var i = 0; i < aLi.length; i++) {
				aClass.push(aLi[i].className)
			};
			//alert(aClass)
			Btn2.onclick=function(){
				aClass.unshift(aClass.pop())
				//alert(aClass)
				for (var i = 0; i < aLi.length; i++) {
					aLi[i].className=aClass[i]
				}
			}
			Btn1.onclick=function(){
				aClass.push(aClass.shift())
				for (var i = 0; i < aLi.length; i++) {
					aLi[i].className=aClass[i]
				}

			}
		}
	</script>
</head>
<body>
	<div>
		<input class="val1" type="button" value="←" />
		<input class="val2" type="button" value="→" />

	</div>
	<ul>
		<li class="first">
			<img src="img/2014cpb1216dotaa07s.jpg">
		</li>
		<li class="left">
			<img src="img/timg (1).jpg">
		</li>
		<li class="conter">
			<img src="img/timg (2).jpg">
		</li>
		<li class="right">
			<img src="img/timg (3).jpg">
		</li>
		<li class="last">
			<img src="img/timg (4).jpg">
		</li>
		<li>
			<img src="img/timg (5).jpg">
		</li>
		<li>
			<img src="img/timg.jpg">
		</li>
		<li>
			<img src="img/u=1012099935,911386843&fm=23&gp=0.jpg">
		</li>
	</ul>
</body>
</html>