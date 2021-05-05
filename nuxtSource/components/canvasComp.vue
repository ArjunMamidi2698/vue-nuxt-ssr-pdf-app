<template>
    <div class="canvas-component-test">
        <div id="chartContainer" style="height: 370px; width: 100%;">
			<canvas></canvas>
		</div>
		<span>{{responseData}}</span>
    </div>
</template>
<script>
// import CanvasJS from 'canvasjs';
// import $ from 'jquery';
export default {
    data() {
        return {
            responseData: null,
        }
    },
    mounted () {
		var dataPoints = [];
		var chart = new CanvasJS.Chart("chartContainer", {
			animationEnabled: true,
			theme: "light2",
			title: {
				text: "Daily Sales Data"
			},
			axisY: {
				title: "Units",
				titleFontSize: 24,
				includeZero: true
			},
			data: [{
				type: "column",
				yValueFormatString: "#,### Units",
				dataPoints: dataPoints
			}]
		});
		function addData(data) {
			this.responseData = data;
			for (var i = 0; i < data.length; i++) {
				dataPoints.push({
					x: new Date(data[i].date),
					y: data[i].units
				});
			}
			chart.render();
		}
		$.getJSON("https://canvasjs.com/data/gallery/javascript/daily-sales-data.json", addData);
	}
}
</script>