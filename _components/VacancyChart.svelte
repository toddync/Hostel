<script>
	//@ts-nocheck
	import Chart from "chart.js";
	import { onMount } from "svelte";

	let values = [20, 10, 5, 2, 20, 30, 45];
	let labels = [
		"January",
		"February",
		"March",
		"April",
		"May",
		"June",
		"July",
	];

	let canvas;

	onMount(async (promise) => {
		let ctx = canvas.getContext("2d");
		Chart.defaults.color = "#000";
		var chart = new Chart(ctx, {
			type: "line",
			data: {
				labels,
				datasets: [
					{
						backgroundColor: "rgba(255, 99, 132, .1)",
						borderColor: "rgb(255, 99, 132)",
						data: values,
					},
				],
			},
			options: {
				legend: {
					display: false,
				},
			},
		});
	});
</script>

<canvas bind:this={canvas} class="my-auto max-h-72" />
