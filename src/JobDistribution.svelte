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
        <h2 style="color: darkmagenta;">Fast and Effective</h2>
        <p style="color:black; font-weight: 700;">Stop wasting time posting to tens of job boards manually, advertise</p>
        <p>your vacancies to multiple job boards, social media, and to your.</p>
        
      
      </div>
      <h style="color:yellow; ">Simplified Applicant Management</h>
      <section class="testimonials-section">
       
          <div class="container">
           <h6>Jobs are posted automatically to job boards with the link to apply in the ATS. Applicants create their account and</h6>
           <h6>your vacancies to multiple job boards, social media, and to your website instantly.</h6>
                </div>
              </div>

<h style="color:red; ">Measure Performance</h>
      <section class="testimonials-section">
       
          <div class="container">
           <h6>Post your job adverts to job boards and social media channels instantly with Recruitly job posting tool.</h6>
        <img   width="600" height="600"  src=https://recruitly.io/wp-content/uploads/2021/01/measure-performance.png />
      
                </div>
              </div>
             
             
   </section>
  
  
  <style>
    .spacer {
      margin: 0 10px;
    }
    .hero-section {
    text-align: center;
    margin-top: -1300px;
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
  
