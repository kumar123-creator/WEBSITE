<script>
import { createEventDispatcher } from 'svelte';    
import 'bootstrap/dist/css/bootstrap.min.css';
import { Link } from "svelte-routing";
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
  
  <section class="recruiting-tracking-section">
    <div class="links">
      <nav>
        <ul >
          <a on:click={openWhyRecruitlyPopup} class="why-recruitly-anchor" style="color: blue; font-weight: 700;">Why Recruitly</a>
          <span class="spacer"></span>
          <li><Link to="/automation" style="color:blue; font-weight: 700;">Automation</Link></li>
          <span class="spacer"></span>
          <li><Link to="/pricing" style="color:blue; font-weight: 700;">Pricing</Link></li>
        </ul>
      </nav>
    </div>
    <div class="tracking-component">
      <div class="hero-section">
        <h2 style="color: darkmagenta;">Simple and Easy to Use</h2>
        <p style="color:black; font-weight: 700;">Recruitly Applicant Tracking Software is designed to boost recruiters productivity </p>
        <p>with UI that’s easy to navigate and lightning fast.</p>
        </div>
 
<h2 style="color: blue;">Candidate Portal</h2>
 <section class="testimonials-section">
<div class="container">
 <p>Stay GDPR compliant by offering candidates full control over their consent and privacy settings, and full audit visibility..</p>
</div>


      <h style="color:blue; ">More Features</h>
      <section class="testimonials-section">
        <table>
          <div class="container">
            <div class="row">
              <div class="col-md-4">
                <div class="feature-card">
                  <i class="fa fa-search"></i>
                  <img  src="https://recruitly.io/wp-content/uploads/2020/12/engage2-150x150.png"  />
                  <h3 style="color:blue; font-weight:600;">Reach & Engage</h3>
                  <h6>Create an unbeatable candidate and client experience by initiating and maintaining a one-on-one dialogue directly from your Recruitly account and reduce time and cost to fill.
                </h6>
                </div>
              </div>
              <div class="col-md-4">
                <div class="feature-card">
                  <i class="fa fa-envelope"></i>
                  <img src=https://recruitly.io/wp-content/uploads/2020/12/interviewschedule2-150x150.png />
                  <h3 style="color:blue; font-weight:600;">Take Charge</h3>
                  <h6>Create an unbeatable candidate and client experience by initiating and maintaining a one-on-one dialogue directly from your Recruitly account and reduce time and cost to fill..</h6>
                </div>
              </div>
              <div class="col-md-4">
                <div class="feature-card">
                  <i class="fa fa-users"></i>
                  <img src=	https://recruitly.io/wp-content/uploads/2020/12/starplacement2-150x150.png />
                  <h3 style="color:blue; font-weight:600;">More Placements</h3>
                  <h6>From job posting to placement management – Recruitly offers all the tools you need to successfully operate your recruitment business and to be productive and make more placements.</h6>
                </div>
              </div>
             
            </div>
          </div>
        </table>
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
  .recruiting-tracking-section h{
     
     font-weight: bold;
     font-size: 2rem;
     margin-top: 80px;
   }
    .recruiting-tracking-section h2 {
        margin-top: 1px;
    margin-bottom: 1px;
      font-weight: bold;
      font-size: 3rem;
    }
    .recruiting-tracking-section p {
     
      font-weight: bold;
      font-size: 1.5rem;
    }
  
    .recruiting-tracking-section h3 {
  
      font-weight: bold;
      font-size: 1.7rem;
      margin-top: 50px;
    }
    .recruiting-tracking-section h6 {
  
    font-weight: bold;
    font-size: 1rem;
    margin-top: 10px;
   }
  
  
  
   
    
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }
  
    .tracking-component {
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
   
  
   
  
    .tracking-component ul {
      list-style-type: disc;
      margin-left: 20px;
    }
  
    .tracking-component li {
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
  
