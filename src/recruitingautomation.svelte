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
    <section class="hero-section">
      <h2 style="color: darkmagenta;">Recruiting Automation</h2>
      <p style="color: black; font-weight: 300;">Increase efficiency by creating workflows that automate repetitive and common tasks, save hours each day.</p>
      <p style="color: black; font-weight: 500;">Recruiting automation allows you to focus on the work that matters!</p>
      <p style="color: black; font-weight: 300;">Automation can be key to recruiting efficiency, but only if done right. It takes time and effort to create the right workflow that is optimal for your business. Our intuitive automation platform allows you to configure the triggers, actions, and amend them when necessary with ease.</p>
    </section>
  
    <section class="automation-reasons-section">
      <h3 style="color: blue; text-align: center; margin-bottom: 20px;">Why Automate</h3>
  
      <div class="testimonials-section">
        <div class="feature-card">
          <i class="fa fa-search"></i>
          <h4 style="color: purple; font-weight: 600;">Save time</h4>
          <p>Increase efficiency by creating workflows that automate repetitive and common tasks, save hours each week.</p>
        </div>
        <div class="feature-card">
          <i class="fa fa-users"></i>
          <h4 style="color: purple; font-weight: 600;">Be in control</h4>
          <p>Ensure that recruiting standards are enforced automatically, and build a streamlined and error-proof workflow.</p>
        </div>
        <div class="feature-card">
          <i class="fa fa-cogs"></i>
          <h4 style="color: purple; font-weight: 600;">Automate everything</h4>
          <p>Automate every step of your recruiting process, from sourcing to onboarding, and save valuable time and effort.</p>
        </div>
      </div>
    </section>
  </div>
</section>

<style>
  .spacer {
    margin: 0 10px;
  }

  .recruiting-automation-section h2 {
    font-weight: bold;
    font-size: 3rem;
    margin-bottom: 10px;
    margin-top: 0;
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
    margin-top: 5vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    padding: 20px;
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
    top: 8px;
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

  .hero-section {
    text-align: center;
    margin-bottom: 10px;
  }

  .automation-reasons-section {
    text-align: center;
    margin-top: 30px;
  }

  .automation-reasons-section h3 {
    color: blue;
    font-weight: bold;
    font-size: 2rem;
    margin-top: 80px;
  }

  .testimonials-section {
    display: flex;
    justify-content: space-between;
    margin-top: 30px;
  }

  .feature-card {
    width: 30%;
    text-align: center;
  }

  .feature-card i {
    font-size: 3rem;
    margin-bottom: 10px;
    color: purple;
  }

  .feature-card h4 {
    color: purple;
    font-weight: 600;
    font-size: 1.7rem;
    margin-top: 50px;
  }

  .feature-card p {
    color: black;
    font-weight: 600;
    font-size: 1rem;
    margin-top: 10px;
  }
</style>
