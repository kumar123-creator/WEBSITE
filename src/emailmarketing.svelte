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

<section class="recruiting-email-section">
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
 <div class="email-component">
    <div class="hero-section">
      <h2 style="color: darkmagenta;">Recruitment Email Marketing</h2>
      <p style="color:black; font-weight: 700;">Reach your audience and improve your branding, with an email marketing solution </p>
      <p style="color:black; font-weight: 600;">built right into  recruitment database.</p>
    
    </div>
    <img src = https://recruitly.io/wp-content/uploads/2020/11/personalised-templates.png />

<p style="color:green; font-weight: 900;">Measure Performance</p>
<p style="color:black; font-weight: 700;">You can track everything from who opened and clicked your campaigns, health of your email lists and performance of your campaigns and segments.</p>
<p style="color:black; font-weight: 600;">Gain valuable insights to shape your email marketing strategies.</p>
  
    <section class="testimonials-section">
      <table>
        <div class="container">
          <div class="row">
            <div class="col-md-4">
              <div class="feature-card">
                <i class="fa fa-search"></i>
                <h3 style="color:purple; font-weight:600;">Email Campaigns</h3>
                <h6>Send e-shots directly from Recruitly, and create stunning campaigns for lead generation and engagement.
              </h6>
              </div>
            </div>
            <div class="col-md-4">
              <div class="feature-card">
                <i class="fa fa-envelope"></i>
                <h3 style="color:purple; font-weight:600;">Email Templates</h3>
                <h6>Create branded and re-usable email templates with our easy-to-use HTML editor.</h6>
              </div>
            </div>
            <div class="col-md-4">
              <div class="feature-card">
                <i class="fa fa-users"></i>
                <h3 style="color:purple; font-weight:600;">Distribution Lists</h3>
                <h6>Create static distribution lists or link with one of your saved searches..</h6>
              </div>
            </div>
            <div class="col-md-4">
              <div class="feature-card">
                <i class="fa fa-users"></i>
                <h3 style="color:purple; font-weight:600;">Bounce Check</h3>
                <h6>We safeguard your sender reputation by validating emails and checking for bounces before actually sending..</h6>
              </div>
            </div>
            <div class="col-md-4">
              <div class="feature-card">
                <i class="fa fa-users"></i>
                <h3 style="color:purple; font-weight:600;">Dedicated IP</h3>
                <h6>You can opt for a dedicated IP address to take full control of emails sent from your IP to increase inbox placements.
                  .</h6>
              </div>
            </div>
            <div class="col-md-4">
              <div class="feature-card">
                <i class="fa fa-users"></i>
                <h3 style="color:purple; font-weight:600;">Analytics</h3>
                <h6>Provides analytics including applications, job boards, placements and many more that allow you to see which job board works better for your job adverts..</h6>
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
  margin-top: -600px;
  margin-bottom: 10px;
}
.recruiting-email-section h{
   
   font-weight: bold;
   font-size: 2rem;
   margin-top: 80px;
 }
  .recruiting-email-section h2 {
      margin-top: 1px;
  margin-bottom: 1px;
    font-weight: bold;
    font-size: 3rem;
  }
  .recruiting-email-section p {
   
    font-weight: bold;
    font-size: 1.5rem;
  }

  .recruiting-email-section h3 {

    font-weight: bold;
    font-size: 1.7rem;
    margin-top: 50px;
  }
  .recruiting-email-section h6 {

  font-weight: bold;
  font-size: 1rem;
  margin-top: 10px;
 }



 
  
  body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
  }

  .email-component {
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
