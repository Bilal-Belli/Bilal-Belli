<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.0.0/dist/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.12.9/dist/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.0.0/dist/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
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

