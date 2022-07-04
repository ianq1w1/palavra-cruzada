<svelte:head>
	<link rel="stylesheet" href="/styles/Jogostyle.css">
</svelte:head>

<script>
	let p1 = "ferradura" // palavra linha da cruzada 
	let p2 = "mercadoria"
	let p3 = "olfato"
	let p4 = "burrada"
	let p5 = "comprar"
	let p6 = "voar"
	let p7 = "ateu"
	let p8 = "roupa"
</script>

<table border="1" align="center"><!-- tabela das cruzadas-->
	<tbody>	
	<tr id="vazio">
	<td id="vazio">	
	</td>       <!--id vazio = espaçamento-->
	<tr>
		{#each Array.from(p5) as coisas}
			<td>	
				<input type="text" id="quadrado">
			</td>
		{/each}
	</tr>
	<tr>
		{#each Array.from(p1) as coisas}<!-- loop each = quadros para escrever-->
			<td>
				<input type="text" id="quadrado">
			</td>
		{/each}
	</tr>
	<tr>
		{#each Array.from(p1) as coisas}
			<td>
				<input type="text" id="quadrado">
			</td>
		{/each}
	</tr>
	<tr>
		{#each Array.from(p2) as coisas}
			<td>
				<input type="text" id="quadrado">
			</td>
		{/each}
	</tr>
	<tr>
		<td>
			<input type="text" id="quadrado">
		</td>
	</tr>
		{#each Array.from(p2) as coisas}
	<tr>
		<input type="text" id="quadrado">
	</tr>
		{/each}
	</tbody>
</table>