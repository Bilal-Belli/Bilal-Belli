<div class="container">
               <div class="row align-items-center">
                  <div class="col-lg-4"><canvas id="ChartSkills"></canvas></div>
                  <div class="col-lg-4"><canvas id="ChartProgrammingLanguages"></canvas></div>
                  <div class="col-lg-4"><table class="table table-bordered table-hover">
                     <thead>
                       <tr>
                         <th>Frameworks</th> 
                       </tr>
                     </thead>
                     <tbody>
                       <tr>
                        <td>Bootstrap V4</td>
                       </tr>
                       <tr>
                         <td>Django</td> 
                       </tr>
                       <tr>
                         <td>Chart.js</td> 
                       </tr>
                       <tr>
                         <td>Angular</td> 
                       </tr>
                       <tr>
                         <td>Node.js</td> 
                       </tr>
                     </tbody>
                   </table></div>
               </div>
            </div>
            
            <script>
            //programming languages chart
var xValuesPL = ["HTML", "CSS", "JavaScript", "Python", "Java", "C", "Pascal"];
var yValuesPL = [100, 80, 60, 80, 50, 90, 70, 0];
new Chart("ChartProgrammingLanguages", {
	type: "horizontalBar",
	data: {
		labels: xValuesPL,
		datasets: [{
			backgroundColor: "#47d1ae",
			data: yValuesPL
		}]
	},
	options: {
		title: {
			display: true,
			text: "Programming Languages Used"
		}, 
        elements: {
			bar: {
				borderWidth: 50,
			}
		},
		legend: {
			display: false
		},
		responsive: true
	}
});
//--------------------------------------------
//skills chart
var xValuesSK = ["Web Developper", "Analyst", "Blogger", "Architecter", "Mobile Developper", "Designer"];
var yValuesSK = [80, 80, 70, 70, 20, 80];
new Chart("ChartSkills", {
	type: "radar",
	data: {
		labels: xValuesSK,
		datasets: [{
			backgroundColor: 'rgba(71, 209, 174, 0.5)',
			data: yValuesSK
		}]
	},
	options: {
		scale: {
			ticks: {
				beginAtZero: true,
				max: 100,
				min: 0,
				stepSize: 10
			}
		},
		legend: {
			display: false
		},
		responsive: true,
		title: {
			display: true,
			text: "Performance"
		}
	}
});
//--------------------------------------------
//frameworks chart
//to work later
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.5.0/Chart.min.js"></script><!--Chart.js-->
