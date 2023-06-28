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
  
  <section class="recruiting-web-section">
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
    <div class="web-component">
      <div class="hero-section">
      
        <h2 style="color: darkmagenta;">Recruitly + WordPress</h2>
       
      </div>
      
     
      
      <section class="testimonials-section">
      
            <i class="fa fa-search"></i>
            <h2 style="color: blue; font-weight:600;">WordPress Plugin</h2>
            <p>Recruitly WordPress plugin establishes a 360 degree integration with your Recruitly database and </p>
            <p>turns your website into a fully featured job-board within a matter of minutes.</p>




   <img src = "https://recruitly.io/wp-content/uploads/2020/11/recruitly_plugin_wordpress.png" alt="Recruitly WordPress Plugin" style="width: 100%; max-width: 500px; margin-bottom: 50px" />





      </section>
             
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
  .testimonials-section{
    margin-top: 50px;
  }
  .recruiting-web-section h{
     
     font-weight: bold;
     font-size: 1rem;
     margin-top: 80px;
   }
    .recruiting-web-section h2 {
        margin-top: 1px;
    margin-bottom: 1px;
      font-weight: bold;
      font-size: 3rem;
    }
    .recruiting-web-section p {
     
      font-weight: bold;
      font-size: 1.5rem;
    }
  
    .recruiting-web-section h3 {

      font-weight: bold;
      font-size: 1.7rem;
      margin-top: 50px;
    }
    .recruiting-web-section h6 {

    font-weight: bold;
    font-size: 1rem;
    margin-top: 10px;
   }
 

  
   
    
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    .web-component {
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
   

   

    .web-component ul {
      list-style-type: disc;
      margin-left: 20px;
    }

    .web-component li {
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
  
