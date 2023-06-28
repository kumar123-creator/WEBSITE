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
  
  <section class="recruiting-chrome-section">
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
    <div class="chrome-component">
      <div class="hero-section">
        <h2 style="color: darkmagenta;">Google Chrome Extension</h2>
        <p style="color:black; font-weight: 700;">Easily source leads, contacts and candidates from LinkedIn and</p>
        <p>other websites using our revolutionary Google Chrome Extension.</p>
        <img   width="400" height="300"  src = https://i0.wp.com/naijaknowhow.net/wp-content/uploads/2023/02/Image-Extension-for-Chrome.png/>
      
      </div>
      <h style="color:blue; ">Source Leads, Contacts and Candidates</h>
      <section class="testimonials-section">
       
          <div class="container">
           <h6>No more back and forth or manual data entry, let Recruitly take care of extracting all the data for you.</h6>
           <h6>With just a single click you can source leads, contacts and candidates and add them to your Recruitly account!.</h6>
           <img   width="600" height="600"  src= https://recruitly.io/wp-content/uploads/2021/09/extension-addnew-1024x1024.png/>
      
          
                </div>
              </div>
             
   </section>
  
  
  <style>
    .spacer {
      margin: 0 10px;
    }
    .hero-section {
    text-align: center;
    margin-top: -500px;
    margin-bottom: 10px;
  }
  .recruiting-chrome-section h{
     
     font-weight: bold;
     font-size: 2rem;
     margin-top: 80px;
   }
    .recruiting-chrome-section h2 {
        margin-top: 1px;
    margin-bottom: 1px;
      font-weight: bold;
      font-size: 3rem;
    }
    .recruiting-chrome-section p {
     
      font-weight: bold;
      font-size: 1.5rem;
    }
  
    .recruiting-chrome-section h3 {
  
      font-weight: bold;
      font-size: 1.7rem;
      margin-top: 50px;
    }
    .recruiting-chrome-section h6 {
  
    font-weight: bold;
    font-size: 1rem;
    margin-top: 10px;
   }
  
  
  
   
    
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }
  
    .chrome-component {
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
   
  
   
  
    .chrome-component ul {
      list-style-type: disc;
      margin-left: 20px;
    }
  
    .chrome-component li {
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
  
