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
            <h2 style="color: blue; font-weight:600;">Drag&Drop</h2>
            <h2 style="color: green; font-weight:600;">Recruitment Websites</h2>
            <p>Recruitly offers a lightweight WordPress plugin to help building recruitment websites faster and for adding</p>
            <p>job-board functionality with just simple clicks. Being WordPress shortcode based, it can work with any</p>
             <p>theme and is really simple to install and configure. Recruitly also offers a line of Elementor and DIVI widgets</p>
             <p>to help you fine-tune your design elements and adjust features, so you can get the most out of your pages.</p>
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
  
