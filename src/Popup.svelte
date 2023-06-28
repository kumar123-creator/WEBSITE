<script>
  export let closePopup;
</script>

<div class="popup" on:click={closePopup}>
  <div class="popup-content">
    <button class="close-button" on:click={closePopup}>&times;</button>
    <div class="popup-section">
      <Route path="/email-marketing">
        <Link to="/email-marketing">
          <h3>Email Marketing</h3>
        </Link>
      </Route>
      <p class="custom-paragraph">Engage talent at the right time, promote your business to the right audience.</p>
    </div>
    <div class="popup-section">
      <Route path="/applicant-tracking-system">
        <Link to="/applicant-tracking-system">
          <h3>Applicant Tracking System</h3>
        </Link>
      </Route>
      <p class="custom-paragraph">Candidate sharing, boolean searches, interview scheduling, automation and more.</p>
    </div>
    <div class="popup-section">
      <Route path="/website-integration">
        <Link to="/website-integration">
          <h3>Website Integration</h3>
        </Link>
      </Route>
      <p class="custom-paragraph">Turn your WordPress website into a fully featured job-board using our FREE plugins.</p>
    </div>
    <div class="popup-section">
      <Route path="/job-distribution">
        <Link to="/job-distribution">
          <h3>Job Distribution</h3>
        </Link>
      </Route>
      <p class="custom-paragraph">Get your job in front of millions of candidates, manage applicants in one place.</p>
    </div>
    <div class="popup-section">
      <Route path="/search-import">
        <Link to="/search-import">
          <h3>Search & Import</h3>
        </Link>
      </Route>
      <p class="custom-paragraph">Search and import candidates from CV-Library and TotalJobs with just a few clicks.</p>
    </div>
    <div class="popup-section">
      <Route path="/recruiting-automation">
        <Link to="/recruiting-automation">
          <h3>Recruiting Automation</h3>
        </Link>
      </Route>
      <p class="custom-paragraph">Boost your team's productivity by creating workflows that automate repetitive and common tasks.</p>
    </div>
  </div>
</div>
  
  <style>
   
    .popup {
	  position: fixed;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  background-color: rgba(0, 0, 0, 0.5);
	  display: flex;
	  justify-content: center;
	  align-items: center;
	}
  
	.popup-content {
	  position: relative; /* Added position relative */
	  background-color: #fff;
	  padding: 20px;
	  text-align: center;
	  border-radius: 5px;
	  width: 80%; /* Increased the width */
	  height: 80%; /* Increased the height */
	  max-width: 800px;
	  display: flex;
	  flex-wrap: wrap;
	  justify-content: center;
	  align-items: center;
	  overflow-y: auto;
	}
  
	.popup-section {
	  width: calc(50% - 20px); 
	  height: 25%; 
	  padding: 10px;
	}
  
	.custom-paragraph {
	  text-align: center; 
	}
  
	.popup-content h3 {
	  text-align: center;
	  color: blue;
	}
  
	.popup-content p.custom-paragraph {
	  width: 100%; /* Set the width for the paragraphs */
	  text-align: center; /* Center the paragraph text */
	}
    .close-button {
	  position: absolute;
	  top: 0px;
	  right: 1px;
	  font-size: 24px;
	  color: #f00f22;
	  background: transparent;
	  border: none;
	  cursor: pointer;
	}
  </style>
  
