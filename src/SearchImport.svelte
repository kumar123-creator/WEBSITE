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
  
  <section class="recruiting-search-section">
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
    <div class="search-component">
      <div class="hero-section">
        <h2 style="color: darkmagenta;">View millions of active candidates
        </h2>
        <p style="color:black; font-weight: 700;">You’re guaranteed to find the freshest talent in your</p>
        <p>industry for your vacancies.</p>
        
      
      </div>
      <h style="color:blue; ">CV Search & Import</h>
      <section class="testimonials-section">
       
          <div class="container">
           <h6>The unique CV Search & Import integration allows all you to access extensive</h6>
           <h6>CV Database of CV-Library and TotalJobs from your Recruitly ATS platform.</h6>
           
           <img src = 	https://recruitly.io/wp-content/uploads/2020/11/cv-search-filters.svg />
                </div>
              </div>
             
   </section>
  
  
  <style>
    .spacer {
      margin: 0 10px;
    }
    .hero-section {
    text-align: center;
    margin-top: -900px;
    margin-bottom: 10px;
  }
  .recruiting-search-section h{
     
     font-weight: bold;
     font-size: 2rem;
     margin-top: 80px;
   }
    .recruiting-search-section h2 {
        margin-top: 1px;
    margin-bottom: 1px;
      font-weight: bold;
      font-size: 3rem;
    }
    .recruiting-search-section p {
     
      font-weight: bold;
      font-size: 1.5rem;
    }
  
    .recruiting-search-section h3 {
  
      font-weight: bold;
      font-size: 1.7rem;
      margin-top: 50px;
    }
    .recruiting-search-section h6 {
  
    font-weight: bold;
    font-size: 1rem;
    margin-top: 10px;
   }
  
  
  
   
    
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }
  
    .search-component {
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
   
  
   
  
    .search-component ul {
      list-style-type: disc;
      margin-left: 20px;
    }
  
    .search-component li {
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
  
