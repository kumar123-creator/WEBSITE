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

<section class="RecruitlyPricing">
  <div class="links">
    <nav>
      <ul>
        <a on:click={openWhyRecruitlyPopup} class="why-recruitly-anchor" style="color: blue; font-weight: 700;">Why Recruitly</a>
        <span class="spacer"></span>
        <li><Link to="/automation" style="color: blue; font-weight: 700;">Automation</Link></li>
        <span class="spacer"></span>
        <li><Link to="/pricing" style="color: blue; font-weight: 700;">Pricing</Link></li>
      </ul>
    </nav>
  </div>

  <div class="pricing-component">
    <div class="hero-section">
      <h1 style="color: blue;">Recruitly Pricing</h1>
      <p>Recruitly is a pay-as-you-go service, excluding 1-Week FREE trial. All payments should be made upfront before using the service.</p>
    </div>

    <section class="compare-section">
      <div class="container-fluid">
        <h1 style="color: red;">Compare Plans</h1>
        <table class="table table-bordered">
          <thead>
            <tr>
              <th></th>
              <th>Solo</th>
              <th>Startup</th>
              <th>Professional</th>
              <th>Enterprise</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Recruitment CRM</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
            </tr>
            <tr>
              <td>Applicant Tracking System</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
            </tr>
            <tr>
              <td>Job Ad Distribution</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
            </tr>
            <tr>
              <td>Email Marketing</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
              <td>✔</td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>

    <section class="features-section">
      <div class="container-fluid mt-4">
        <h1 style="color: orange;">Affordable plans</h1>
         
        <div class="row">
          <div class="col p-3 bg-info text-white" style="color: blue; font-weight: 700;">
            <h1>Solo</h1>
            <p>For independent recruiters</p>
            <p>$35</p>
            <p>/user/month</p>
          </div>
              
          <div class="col p-3 bg-success text-white" style="font-weight: 700;">
            <h1>Startup</h1>
            <p>For startup agencies</p>
            <p>$50</p>
            <p>/user/month</p>
          </div>
          <div class="col p-3 bg-info text-white" style="font-weight: 700;">
            <h1>Professional</h1>
            <p>For established teams</p>
            <p>$75</p>
            <p>/user/month</p>
          </div>
          <div class="col p-3 bg-success text-white" style="font-weight: 700;">
            <h1>Enterprise</h1>
            <p>For large organizations</p>
            <p>$100</p>
            <p>/user/month</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</section>

<style>
  .RecruitlyPricing {
    padding-top: 50px;
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
    margin-right: 5px;
  }
  
  .spacer {
    margin: 0 10px;
  }
  
  .why-recruitly-anchor {
    cursor: pointer;
  }

  .pricing-component {
    margin-top: 5vh;
    width: 220vh;
    height: 250vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: white;
    padding: 20px;
    margin-left: 140vh;
    margin-right: -50vh;
  }

  .pricing-component p {
    font-size: 18px;
    margin-bottom: 10px;
  }

  .pricing-component ul {
    list-style-type: disc;
    margin-left: 20px;
  }

  .pricing-component li {
    font-size: 16px;
    margin-bottom: 5px;
  }

  .hero-section {
    text-align: center;
    margin-top: -1100px;
    margin-bottom: 10px;
  }

  .compare-section {
    margin-top: 30px;
  }

  .compare-section h1 {
    color: red;
    text-align: center;
    font-weight: bold;
    font-size: 3rem;
    margin-top: 10px;
    margin-bottom: 10px;
  }

  .compare-section table {
    margin-top: 30px;
  }

  .compare-section th {
    text-align: center;
    font-weight: bold;
  }

  .compare-section td {
    text-align: center;
  }

  .features-section {
    margin-top: 50px;
  }

  .features-section h1 {
    color: blue;
    font-weight: bold;
    font-size: 2rem;
    margin-top: 10px;
    margin-bottom: 10px;
  }
</style>
