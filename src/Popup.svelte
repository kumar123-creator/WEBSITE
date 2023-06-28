<script>
	import emailmarketing from "./emailmarketing.svelte";
	import { createEventDispatcher} from 'svelte';
	import 'bootstrap/dist/css/bootstrap.min.css';
	import { navigate } from "svelte-routing";
    const dispatch = createEventDispatcher();
	import { Router, Link, Route } from "svelte-routing";
    import TrackingSystem from "./TrackingSystem.svelte";
	import SearchImport from "./SearchImport.svelte";
	
	export let closePopup;

        function navigateToEmail() {
	    window.location.href = "/Emailmarketing";
	    }
		function navigateToTrackingSystem() {
	    window.location.href = "/Tracking_System";
	    }
		function navigateToWebsiteIntegration() {
	    window.location.href = "/Website_Integration";
	    }
		function navigateToJobDistribution() {
	    window.location.href = "/Job_Distribution";
	    }
		function navigateToSearchImport(){
	    window.location.href = "/Search_Import";
	    }
		function navigateToRecruitingAutomation() {
	    window.location.href = "/Chrome_Extension";
	    }


   </script>

 <Router>
	<div class="popup">
		<h3>Why Recruitly?</h3>
		
		 <div class="popup" on:click={closePopup}>
		  
			<div class="popup-content">
			  <button class="close-button" on:click={closePopup}>&times;</button>
			  <div class="popup-section">
				<h3><Link to="/Emailmarketing" class="why-recruitly-anchor" style="color: blue; font-weight:700;">Email Marketing</Link></h3>
				
				<p class="custom-paragraph">Engage talent at the right time, promote your business to the right audience.</p>
			  </div>
			  <div class="popup-section">
				<h3><Link to="/Tracking_System" class="why-recruitly-anchor" style="color: blue; font-weight:700;">Applicant Tracking System</Link></h3>
				<p class="custom-paragraph">Candidate sharing, boolean searches, interview scheduling, automation and more.</p>
			  </div>
			  <div class="popup-section">
				<h3><Link to="/Website_Integration" class="why-recruitly-anchor" style="color: blue; font-weight:700;">Website Integration</Link></h3>
				<p class="custom-paragraph">Turn your WordPress website into a fully featured job-board using our FREE plugins.</p>
			  </div>
			  <div class="popup-section">
				<h3><Link to="/Job_Distribution" class="why-recruitly-anchor" style="color: blue; font-weight:700;">Job Distribution</Link></h3>
				<p class="custom-paragraph">Get your job in front of millions of candidates, manage applicants in one place.</p>
			  </div>
			  <div class="popup-section">
				<h3><Link to="/Search_Import" class="why-recruitly-anchor" style="color: blue; font-weight:700;">Search & Import</Link></h3>
				<p class="custom-paragraph">Search and import candidates from CV-Library and TotalJobs with just a few clicks.</p>
			  </div>
			  <div class="popup-section">
				<h3><Link to="/Chrome_Extension" class="why-recruitly-anchor" style="color: blue; font-weight:700;">Google Chrome Extension</Link></h3>
				<p class="custom-paragraph">Easily source leads, contacts and candidates from LinkedIn and other websites.</p>
			  </div>
			</div>
		  
		
	  </div>
	  
 </Router>
  <style>
  
  .popup {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	background-color: rgba(0, 0, 0, 0.5);
	display: flex;
	justify-content: center;
	align-items: center;
  }
  
  .popup-content {
	position: relative;
	background-color: #fff;
	padding: 20px;
	text-align: center;
	border-radius: 5px;
	width: 80%;
	height: 80%;
	max-width: 800px;
	display: flex;
	flex-wrap: wrap;
	justify-content: center;
	align-items: center;
	overflow-y: auto;
  }
  
  .popup-section {
	width: calc(50% - 20px);
	height: 25%;
	padding: 10px;
  }
  
  .custom-paragraph {
	text-align: center;
  }
  
  .popup-content h3 {
	text-align: center;
	color: blue;
  }
  
  .popup-content p.custom-paragraph {
	width: 100%;
	text-align: center;
  }
  
  .close-button {
	position: absolute;
	top: 0px;
	right: 1px;
	font-size: 24px;
	color: #f00f22;
	background: transparent;
	border: none;
	cursor: pointer;
  }
  .spacer {
	margin: 0 10px;
  }
  
	.container {
	  text-align: center;
	  margin-top: 200px;
	}
	h1.display-4 {
	  font-size: 3.5rem;
	  margin-bottom: 0.5rem;
	  font-stretch: expanded;
	}
	.font-weight-bold {
	  font-weight: bold;
	}
  
	.header {
	  background-color: #f8f9fa;
	  padding: 20px;
	  text-align: center;
	}
  
	.information {
	  position: absolute;
	  top: 40px;
	  right: 270px;
	  display: flex;
	  flex-direction: row;
	  align-items: center;
	}
  
	.information p {
	  margin: 0;
	  margin-left: 10px;
	  cursor: pointer;
	}
  
	.popup {
	  position: fixed;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  background-color: rgba(0, 0, 0, 0.5);
	  display: flex;
	  justify-content: center;
	  align-items: center;
	}
  
	.popup-content {
	  position: relative; /* Added position relative */
	  background-color: #fff;
	  padding: 20px;
	  text-align: center;
	  border-radius: 5px;
	  width: 80%; /* Increased the width */
	  height: 80%; /* Increased the height */
	  max-width: 800px;
	  display: flex;
	  flex-wrap: wrap;
	  justify-content: center;
	  align-items: center;
	  overflow-y: auto;
	}
  
	.popup-section {
	  width: calc(50% - 20px); 
	  height: 25%; 
	  padding: 10px;
	}
  
	.custom-paragraph {
	  text-align: center; 
	}
  
	.popup-content h3 {
	  text-align: center;
	  color: blue;
	}
  
	.popup-content p.custom-paragraph {
	  width: 100%; /* Set the width for the paragraphs */
	  text-align: center; /* Center the paragraph text */
	}
  
	body {
	  background-color: #e2f3fc;
	}
	.close-button {
	  position: absolute;
	  top: 0px;
	  right: 1px;
	  font-size: 24px;
	  color: #f00f22;
	  background: transparent;
	  border: none;
	  cursor: pointer;
	}
	.overview-button {
	  margin-top: 10px;
	  padding: 10px 20px;
	  background-color: yellow;
	  color: black;
	  border: none;
	  border-radius: 5px;
	  font-size: 16px;
	  cursor: pointer;
	  display: flex;
	  align-items: center;
	  margin-left: 700px; /* Add margin from the left side */
	  margin-right: auto; /* Add margin from the right side */
	}
	.popup-video-section {
	  width: 100%;
	  text-align: center;
	}
  
	.popup-video {
	  width: 100%;
	  height: 400px;
	}
  
	.why-recruitly-anchor {
	  cursor: pointer;
	}
   
	.modal {
	  background-color: rgba(0, 0, 0, 0.5); /* Adjust the alpha value to control transparency */
	}
	img {
    position: absolute;
    top: 20px; /* Adjust the top position as needed */
    left: 80px; /* Adjust the left position as needed */
    width: 150px; /* Adjust the width as needed */
    height: auto; /* Maintain aspect ratio */
  }
  
  </style>
