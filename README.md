<!DOCTYPE html>
<html>
	<head>
    	<title>FROGGER REMIX</title>
		<script type="text/javascript" src="easel.js"></script>
    	<script type="text/javascript" src="sound.js"></script>
		<script type="text/javascript">
		var stage;
		var canvas;
		function init(){
			Ticker.setFPS(30);
			Ticker.addListener(window);
			canvas = document.getElementById("canvas");
			stage = new Stage(canvas);
			Ticker.setFPS(30);
			Ticker.addListener(window);
			document.onkeydown = onKeyDown;
			document.onkeyup = onKeyUp;
		}
				function onKeyDown(e){
			if(!e){var e = window.event;}
			
			switch(e.keyCode){
				//left
				case 37: moveLeft = true; moveRight = false;
				break;
				//right
				case 39: moveLeft = false; moveRight = true;
				break;
				//up
				case 38: moveUp = true; moveDown = false;	
				break;
				//down
				case 40: moveDown = true; moveUp = false;
				break;
			}
		}
		function onKeyUp(e){
			if(!e){var e = window.event;}
			
			switch(e.keyCode){
				//left
				case 37: moveLeft = false;
				break;
				//right
				case 39: moveRight = false;
				break;
				//up
				case 38: moveUp = false;	
				break;
				//down
				case 40:moveDown = false;
				break;
			}
		}
		</script>
    </head>        
	<body onLoad="init();" style="background-color:#666;">
    
    	<div id="wrapper" style="width:640px; height:480px;
        			  margin-left:auto; margin-right:auto;
            		  background-color:#000000; border:5px ridge #cc8811">
            
					
				<canvas id ="canvas" width=640 height=480
        				  style= "margin-left:auto; margin-right:auto;">
        			</canvas>
        </div>
	</body>
</html>                 
