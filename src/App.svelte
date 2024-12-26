<script>
	import Counter from './counter.svelte'
	let count = 0
	let something;

	$: something = count == 0 ? "Counter" : count;

</script>

<body id="home">
	
	<div id="counteer">
		<div id="overlay">
			<Counter bind:count></Counter>
		</div>
		
		
		<h1 id = "countlogo" class:move = {count != 0} class:unhide = {count != 0}>Counter</h1> <!--  the counter "logo"  --> 
		<h1 id="count">{something}</h1> <!--  the counter text  --> 
		
	</div>
	
	
</body>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		height: 100%;
		background-color: #212120; 
		background-image: linear-gradient(90deg, rgba(89, 89, 89, 0.2) 1px, transparent 1px), linear-gradient(rgba(89, 89, 89, 0.2) 1px, transparent 1px);
		background-size: 70px 70px;
	}

	#counteer {
		color: white;
		text-align: center;
		padding-top: 20%;	
		
	}

	
	#count {
		padding-top: 40px;
		font-size: 60px;
		
	}

	#countlogo {
		color: white;
		transition: all 0.4s ease; 
		font-size: 45px;
		margin-top: 0px;
		display: none;
	}

	.move {
		position: absolute;
		top: 0;
		left: 0;
		transform: translate(20px, 20px);
		font-size: 30px;
	}

	.unhide {
		display: block !important;
	}

	#overlay {
		position: absolute;
		width: 100%;
		height: 100%;
		margin-top: -20%;
	}
	
	
</style>
