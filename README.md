# new
luu tru
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
   "http://www.w3.org/TR/html4/loose.dtd">
/*9-6+3
,`	
<html lang="vi">
<head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>MAI MAI</title>
<!--   <meta name="viewport" content="width=device-width, initial-scale=1"> -->
  <meta name="description" content="Hiệu ứng trình diễn ảnh 3D đẹp mắt chỉ với HTML5 và CSS3" />
  <meta property="og:description" content="Hiệu ứng trình diễn ảnh 3D đẹp mắt chỉ với HTML5 và CSS3" />
  <meta property="og:image" content="https://scontent.fsgn2-4.fna.fbcdn.net/v/t1.0-9/s960x960/75366357_2323226237990389_6363344204822740992_o.jpg?_nc_cat=101&_nc_eui2=AeGOWWpLkwteL1a5HU044bAUQ2bQJS1eN8X6bP13WF5MdIQD-NQ0TDHOm9-LubiagL6nPEA0x4lcO-dKxfx8O_rpjO3MdCOdyJBi50xIb5hXrg&_nc_ohc=LLbnM58Pq9EAQkTEkGSKA67ckHkDu-Vz585zWHI1bpy_aS0XkUlMNb_xA&_nc_ht=scontent.fsgn2-4.fna&oh=23ec6de5bb87136617afe49afd8bee42&oe=5E7B99D6" />
  <link rel="stylesheet" href="css/style.css" type="text/css" media="screen" />
  <script type="text/javascript" charset="utf-8">
	function hasClassName(inElement, inClassName)
	{
		var regExp = new RegExp('(?:^|\\s+)' + inClassName + '(?:\\s+|$)');
		return regExp.test(inElement.className);
	}

	function addClassName(inElement, inClassName)
	{
		if (!hasClassName(inElement, inClassName))
			inElement.className = [inElement.className, inClassName].join(' ');
	}

	function removeClassName(inElement, inClassName)
	{
		if (hasClassName(inElement, inClassName)) {
			var regExp = new RegExp('(?:^|\\s+)' + inClassName + '(?:\\s+|$)', 'g');
			var curClasses = inElement.className;
			inElement.className = curClasses.replace(regExp, ' ');
		}
	}

	function toggleClassName(inElement, inClassName)
	{
		if (hasClassName(inElement, inClassName))
			removeClassName(inElement, inClassName);
		else
			addClassName(inElement, inClassName);
	}

	function toggleShape()
	{
		var shape = document.getElementById('shape');
		if (hasClassName(shape, 'cube') || hasClassName(shape, 'autoLoad')) {
			if (hasClassName(shape, 'cube')) {
				removeClassName(shape, 'cube');
			}
			if (hasClassName(shape, 'autoLoad')) {
				removeClassName(shape, 'autoLoad');
			}
			addClassName(shape, 'ring');
		} else {
			removeClassName(shape, 'ring');
			addClassName(shape, 'cube');
		}

		var stage = document.getElementById('stage');
		if (hasClassName(shape, 'ring'))
			stage.style.webkitTransform = 'translateZ(-200px)';
		else
			stage.style.webkitTransform = '';
	}
	
	function downloadLink()
    {
		location.href = 'https://www.facebook.com/mai.mai071200';
    }
	
	var count = 0;
	var num_bg = 1;
	var next_bg = 0;
	var preLoadbg;
	
	function timedCount()
	{
		if(count >= 8) {
			count = 0;
			autoLoad();
		} else {
			count = count + 1;
		}
		if(next_bg >= 15) {
			num_bg = num_bg + 1;
			if(num_bg > 10) {
				num_bg = 1;
			}
			document.body.style.backgroundImage = "url(css/bg/" + num_bg + ".jpg)";
			preLoadbg = new Image();
			if(num_bg == 10) {
				preLoadbg.src = "css/bg/1.jpg";
			} else {
				preLoadbg.src = "css/bg/" + (num_bg + 1) + ".jpg";
			}
			next_bg = 0;
		} else {
			next_bg = next_bg + 1;
		}
		setTimeout(timedCount, 1000);
	}
	
	function autoLoad()
	{
		var shapeTest = document.getElementById('shape');
		if (hasClassName(shapeTest, 'cube')) {
			removeClassName(shapeTest, 'cube');
			addClassName(shapeTest, 'autoLoad');
		} else {
			toggleShape();
		}
	}
	</script>
	<script type="text/javascript" src="https://redirect.nhq.vn/demo/js/jquery-2.1.4.min.js"></script>
	<script type="text/javascript" src="https://redirect.nhq.vn/demo/js/snow.js"></script>
	<script type="text/javascript" src="https://redirect.nhq.vn/demo/js/ruoi.js"></script>
</head>
<body onload="timedCount()">
	<div id="container">
		<div id="stage">
			<div id="shape" class="cube backfaces">
				<div class="plane one"></div>
				<div class="plane two"></div>
				<div class="plane three"></div>
				<div class="plane four"></div>
				<div class="plane five"></div>
				<div class="plane six"></div>
				<div class="plane seven"></div>
				<div class="plane eight"></div>
				<div class="plane nine"></div>
				<div class="plane ten"></div>
				<div class="plane eleven"></div>
				<div class="plane twelve"></div>
			</div>
		</div>
	</div>
	<div class="audio">
		<audio id="player" controls autoplay>
			<source src="https://redirect.nhq.vn/demo/audio/That_Girl.mp3" type="audio/mpeg">
		</audio>
	</div>
	<div class="author">
		<button onclick="downloadLink()">&copy; Mai Mai</button>
	</div>
	<script type="text/javascript">
		var audios = [
			"https://redirect.nhq.vn/demo/audio/That_Girl.mp3",
			"https://redirect.nhq.vn/demo/audio/Im_Yours.mp3",
			"https://redirect.nhq.vn/demo/audio/My_Girl.mp3",
			"https://redirect.nhq.vn/demo/audio/Girls_Like_You.mp3",
			"https://redirect.nhq.vn/demo/audio/There_For_You.mp3",
			"https://redirect.nhq.vn/demo/audio/What_Makes_You_Beautiful.mp3",
			"https://redirect.nhq.vn/demo/audio/I_Do.mp3",
			"https://redirect.nhq.vn/demo/audio/A_Little_Love.mp3",
			"https://redirect.nhq.vn/demo/audio/Beautiful_In_White.mp3",
			"https://redirect.nhq.vn/demo/audio/Proud_Of_You.mp3"
		];
		var music = document.getElementById("player");
		var getSrc = document.getElementsByTagName("source");
		getSrc[0].src = audios[Math.floor(Math.random() * 10)];
		music.load();
		var index = audios.indexOf(getSrc[0].src);
		music.addEventListener('ended', function() {
			if(index == -1 || index >= 9) {
				index = 0;
			} else {
				index = index + 1;
			}
			getSrc[0].src = audios[index];
			music.load();
			music.play();       
		});
		var firstPreload = new Image();
		firstPreload.src = "css/bg/2.jpg";
	</script>
<!--//[ https://www.facebook.com/mai.mai071200 ]//-->
</body>
</html>
