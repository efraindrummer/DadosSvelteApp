<script>
	let leftSide = "assets/img/dice1.png";
	let rightSide = "assets/img/dice2.png";

	let number1 = 1;
	let number2 = 2;

	function rollCubues() {
		number1 = Math.floor(Math.random() * 6) + 1;
		number2 = Math.floor(Math.random() * 6) + 1
		leftSide = 'assets/img/dice' + number1 + '.png';
		rightSide = 'assets/img/dice' + number2 + '.png';
	}
</script>

<main class="cubes">
	<div class="jumbotron text-center">
		<button class="btn btn-warning lg" on:click={rollCubues}>Tirar Dados</button>
		<br>
		<img src={leftSide} alt="Dado 1" class="img">
		<img src={rightSide} alt="Dado 2" class="img">
		{
			#if number1 == number2
		}
		<h1 class="mt-5">Ganaste los lados son Iguales</h1>
		{
			/if
		}
	</div>
</main>

<style>
	.jumbotron{
		background: #fe8c00;  /* fallback for old browsers */
		background: -webkit-linear-gradient(to right, #f83600, #fe8c00);  /* Chrome 10-25, Safari 5.1-6 */
		background: linear-gradient(to right, #f83600, #fe8c00); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
	}
	.img{
		width: 250px;
		height: 250px;
		background-color: rgb(255, 145, 0);
		margin: 30px;
		border-radius: 20px;
	}
	.cubes{
		height: 100vh;
		background-color: #f83600;
	}
</style>