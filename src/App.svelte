<script>
	import { createEventDispatcher} from 'svelte';
	import 'bootstrap/dist/css/bootstrap.min.css';
	import { navigate } from "svelte-navigator";
	import { Router, Link, Route } from "svelte-routing";
	import RecruitingAutomation from "./recruitingautomation.svelte";
	import RecruitingPricing from "./recruitingpricing.svelte";
        import Popup from './Popup.svelte';

  const dispatch = createEventDispatcher();

   let isPopupOpen = false;
   let showOverviewPopup = false;

  function openWhyRecruitlyPopup() {
  isPopupOpen = true;
    }
  dispatch('openWhyRecruitlyPopup', { closePopup });

  let featureIndex = 0;
	const features = [
	  { text: 'ATS', color: 'blue' },
	  { text: 'CRM', color: 'green' },
	  { text: 'Marketing', color: 'purple' }
	];

     function closePopup() {
     isPopupOpen = false;
	    showOverviewPopup = false;
	  }


	function openOverview() {
	 showOverviewPopup = true;
	}

	setInterval(() => {
	  featureIndex = (featureIndex + 1) % features.length;
	}, 2000);
  
	function navigateToAutomation() {
    window.location.href =  "/automation";
	}
  
	function navigateToPricing() {
    window.location.href ="/pricing";
	}
   
  </script>
   {#if isPopupOpen}
   <Popup {closePopup} />
     {/if}
   
  <main>
  
	<div class="information">
	  <a on:click={openWhyRecruitlyPopup}  class="why-recruitly-anchor" style="color: blue; font-weight: 700;">Why Recruitly</a>
	  <span class="spacer"></span>
    <Router>
      <a on:click={navigateToAutomation} class="why-recruitly-anchor" style="color: blue; font-weight: 700;">Automation</a>
      <span class="spacer"></span>
      <a on:click={navigateToPricing} class="why-recruitly-anchor" style="color: blue; font-weight: 700;">Pricing</a>
      <Route path="/automation" component={RecruitingAutomation} />
      <Route path="/pricing" component={RecruitingPricing} />
    </Router>
	  </div>

 <img src="https://recruitly.io/wp-content/uploads/2020/10/recruitly-logo-300x83.png" onclick="window.location.href='/'" />

<div class="container">
	  <h1 class="display-4"style="color:blue;font-weight: 700;" >Welcome To Recruitment</h1>
	   <h1 class="display-4"style="color:blue;font-weight: 700;"><span class="feature-text" style="color: {features[featureIndex].color}; font-weight: 700;">
		{features[featureIndex].text}
	  </span>
	  System</h1>
		 <p class="card-text">Recruitly® is built to streamline agency recruitment processes and help businesses grow as a result.</p>
	</div>
	<div class="overview-button-container">
	  <button class="overview-button" on:click={openOverview}>Overview</button>
	</div>
	<section class="features-section">
	  <div class="container">
		<div class="row">
		  <div class="col-md-4">
			<div class="feature-card">
			  <i class="fa fa-search"></i>
			  <h3 style="color:black; font-weight: 700;">Powerful Search</h3>
			  <p>Efficiently search and filter through a large pool of candidates.</p>
			</div>
		  </div>
		  <div class="col-md-4">
			<div class="feature-card">
			  <i class="fa fa-envelope"></i>
			  <h3 style="color:yellow;font-weight: 700;">Email Integration</h3>
			  <p>Seamlessly integrate with your email client for easy communication.</p>
			</div>
		  </div>
		  <div class="col-md-4">
			<div class="feature-card">
			  <i class="fa fa-users"></i>
			  <h3 style="color:red;font-weight: 700;">Collaborative Hiring</h3>
			  <p>Collaborate with your team to make better hiring decisions.</p>
			</div>
		  </div>
		</div>
	  </div>
	</section>
  
	<section class="testimonials-section">
	  <div class="container">
		<div class="row">
		  <div class="col-md-6 offset-md-3">
			<h2 style="color:orange;font-weight: 1000;">Faster, Smarter and Effective Recruitment CRM</h2>
			<div class="testimonial">
			  <p>Recruit faster and smarter with our customisable pipelines, built-in job posting and out-of-the-box integrations with the tools you already use and love.</p>
			 
			</div>
		  </div>
		</div>
	  </div>
	</section>
  
	
	<section class="testimonials-section">
	  <div class="container">
		<div class="row">
		  <div class="col-md-6 offset-md-3">
			<h2 style="color:purple;font-weight: 700;">What Our Clients Say</h2>
			<div class="testimonial">
			  <p>"Recuitly.io has transformed our hiring process. We found the perfect candidates in no time."</p>
			  <p class="testimonial-author">John Doe, CEO at ABC Company</p>
			</div>
		  </div>
		</div>
	  </div>
	</section>
	
	<footer class="footer-section">
	  <div class="container">
		<div class="row">
		  <div class="col-md-6">
			<p style="font-weight: 700;">&copy; 2023 Recuitly.io. All rights reserved.</p>
		  </div>
		  
		</div>
	  </div>
	</footer>
  
	
	 </main>
  
   
  
  {#if showOverviewPopup}
	<div class="popup" on:click={closePopup}>
	  <div class="popup-content">
		<button class="close-button" on:click={closePopup}>&times;</button>
		<div class="popup-video-section">
		  <iframe class="popup-video" src="https://www.youtube.com/embed/9L0fVJb7zSk" frameborder="0" allowfullscreen></iframe>
		</div>
	  </div>
	</div>
  {/if}
  
  
	  
 
  
  <style>
	
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
  
  
	
  </style>
  
