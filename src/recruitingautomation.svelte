<script>
    import 'bootstrap/dist/css/bootstrap.min.css';
    import { Link } from "svelte-routing";
    import { createEventDispatcher } from 'svelte';
    import Popup from './Popup.svelte';
  
    let isPopupOpen = false;
    const dispatch = createEventDispatcher();
  
    function openWhyRecruitlyPopup() {
      isPopupOpen = true;
    }
  
    function closePopup() {
      isPopupOpen = false;
    }
  
    dispatch('openWhyRecruitlyPopup', { closePopup });
  </script>
  
  {#if isPopupOpen}
    <Popup {closePopup} />
  {/if}
  
  <section class="recruiting-automation-section">
    <div class="links">
      <nav>
        <ul>
          <a on:click={openWhyRecruitlyPopup} class="why-recruitly-anchor" style="color: blue; font-weight: 700;">Why Recruitly</a>
          <span class="spacer"></span>
          <li><Link to="/automation" style="color:blue; font-weight: 700;">Automation</Link></li>
          <span class="spacer"></span>
          <li><Link to="/pricing" style="color:blue; font-weight: 700;">Pricing</Link></li>
        </ul>
      </nav>
    </div>
    <div class="automation-component">
      <div class="hero-section">
        <h2 style="color: darkmagenta;">Recruiting Automation</h2>
  <p style="color:black; font-weight: 300;">Increase efficiency by creating workflows that automate repetitive and common tasks, save hours each day.</p>
  <p style="color:black; font-weight: 500;">Recruiting automation allows you to focus on the work that matters!</p>
  <p style="color:black; font-weight: 300;">Automation can be key to recruiting efficiency, but only if done right. It takes time and effort to create the right workflow that is optimal for your business. Our intuitive automation platform allows you to configure the triggers, actions and amend them when necessary with ease.</p>
        </div>
 <img src="https://recruitly.io/wp-content/uploads/2021/08/automation-header.svg" alt="Recruiting Automation Image" style="width: 100%; max-width: 500px; margin-bottom: 20px;">
      <h style="color:blue; ">Why Automate</h>
       <section class="testimonials-section">
      <div class="feature-card">
        <i class="fa fa-search"></i>
        <h3 style="color:purple; font-weight:600;">Save time</h3>
        <h6>Increase efficiency by creating workflows that automate repetitive and common tasks, save hours each week.</h6>
      </div>
      <div class="feature-card">
        <i class="fa fa-users"></i>
        <h3 style="color:purple; font-weight:600;">Be in control</h3>
        <h6>Ensure that recruiting standards are enforced automatically, and build a streamlined and error-proof workflow.</h6>
      </div>
      <div class="feature-card">
        <i class="fa fa-cogs"></i>
        <h3 style="color:purple; font-weight:600;">Automate everything</h3>
        <h6>Automate every step of your recruiting process, from sourcing to onboarding, and save valuable time and effort.</h6>
      </div>
    </section>
    </div>
  </section>
  
  <style>
    .spacer {
      margin: 0 10px;
    }
    .hero-section {
    text-align: center;
    margin-top: -1100px;
    margin-bottom: 10px;
  }
  .recruiting-automation-section h{
     
     font-weight: bold;
     font-size: 2rem;
     margin-top: 80px;
   }
    .recruiting-automation-section h2 {
        margin-top: 1px;
    margin-bottom: 1px;
      font-weight: bold;
      font-size: 3rem;
    }
    .recruiting-automation-section p {
     
      font-weight: bold;
      font-size: 1.5rem;
    }
  
    .recruiting-automation-section h3 {

      font-weight: bold;
      font-size: 1.7rem;
      margin-top: 50px;
    }
    .recruiting-automation-section h6 {

    font-weight: bold;
    font-size: 1rem;
    margin-top: 10px;
   }
 

  
   
    
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    .automation-component {
       margin-top:5vh;
      width: 215vh;
      height:250vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background-color:white;
      padding: 20px;
      margin-left: 140vh;
      margin-right: -50vh;
    }

    .why-recruitly-anchor {
	  cursor: pointer;
	}
   

   

    .automation-component ul {
      list-style-type: disc;
      margin-left: 20px;
    }

    .automation-component li {
      font-size: 10px;
      margin-bottom: 5px;
    }
    
    .links {
    display: flex;
    justify-content: flex-end;
    position: absolute;
    top:8px;
    right: 10px;
  }
  
  .links ul {
    display: flex;
    list-style-type: none;
    padding: 0;
  }
  
  .links li {
    margin-right: 0px;
  }

   
  </style>
  
