
<!-- CUSTOM COLOR OVERRIDES: DEEP BURGUNDY, RED & BLUE ACCENTS -->
<style>
  /* Changes the main header to a deep burgundy gradient */
  .page-header {
    background-image: linear-gradient(120deg, #4a0e17, #1a0003) !important;
    background-color: #4a0e17 !important;
  }
  
  /* Vibrant blue highlights for headings */
  h1, h2, h3, h4 {
    color: #2563eb !important; /* Vibrant Blue */
  }
  
  /* Vibrant red/burgundy accents for links */
  a {
    color: #dc2626 !important; /* Vibrant Red */
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
    color: #b91c1c !important;
  }
  
  /* Customizing the header buttons to match your theme */
  .btn {
    color: rgba(255, 255, 255, 0.8) !important;
    border-color: rgba(255, 255, 255, 0.3) !important;
    background-color: rgba(220, 38, 38, 0.2) !important; /* Subtle Red tint */
  }
  .btn:hover {
    background-color: rgba(37, 99, 235, 0.3) !important; /* Vibrant Blue hover */
    border-color: rgba(255, 255, 255, 0.5) !important;
  }
</style>


# Hello, I'm a Computer Science Student at UWEC! 

Welcome to my software development portfolio! I am currently a student at the **University of Wisconsin-Eau Claire**, diving deep into the fundamentals of computer science and modern programming workflows.

---

##  Navigation
**About Me (Home)** | [My Learning Journey](projects.md) | [Future Coursework & Goals](future-work.md)

---

##  Skills I Am Building
I am currently focusing on mastering core programming concepts, logical problem-solving, and professional developer workflows.

### Academic Focus
* **Algorithmic Thinking:** Breaking down word problems into step-by-step logic.
* **Developer Workflows:** Mastering the Git version control system and the GitHub platform.
* **Technical Writing:** Documenting code and processes cleanly for team collaboration.

---

##  My Objective
My goal is to build a rock-solid foundation in software engineering principles here at UWEC. I am looking to connect with peers, learn from faculty, and prepare myself for future technical internships.

<!-- CONTROL FLOW INTERACTIVE WIDGET -->
<div style="background-color: #0f172a; color: #f8fafc; padding: 25px; border-radius: 12px; margin-top: 30px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; border: 2px solid #a855f7; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);">
  <h3 style="color: #a855f7; margin-top: 0;">⚙️ Control Flow & Loop Simulator</h3>
  <p style="color: #94a3b8; font-size: 0.95rem;">Select an execution block to dynamically simulate how a compiler processes loops and conditional branches:</p>
  
  <!-- Interactive Navigation Tabs -->
  <div style="display: flex; gap: 8px; margin-bottom: 15px;">
    <button onclick="runControl('if/else')" style="flex: 1; background-color: #1e293b; color: #3b82f6; border: 1px solid #3b82f6; padding: 8px; font-weight: bold; border-radius: 6px; cursor: pointer;">If/Else</button>
    <button onclick="runControl('for')" style="flex: 1; background-color: #1e293b; color: #a855f7; border: 1px solid #a855f7; padding: 8px; font-weight: bold; border-radius: 6px; cursor: pointer;">For Loop</button>
    <button onclick="runControl('while')" style="flex: 1; background-color: #1e293b; color: #10b981; border: 1px solid #10b981; padding: 8px; font-weight: bold; border-radius: 6px; cursor: pointer;">While Loop</button>
  </div>

  <!-- Terminal Display Window -->
  <div style="background: #020617; padding: 12px; border-radius: 6px; border: 1px solid #334155; font-family: 'Courier New', Courier, monospace; min-height: 80px; font-size: 0.9rem;">
    <span style="color: #64748b;">// Console Output Window</span>
    <div id="terminalOutput" style="color: #38bdf8; margin-top: 8px;">Click a control module tab above to execute the simulation console...</div>
  </div>
</div>

<!-- JAVASCRIPT SIMULATOR CONTROLLER -->
<script>
  function runControl(type) {
    let output = document.getElementById('terminalOutput');
    output.innerHTML = '';
    
    if (type === 'if/else') {
      let grade = 88;
      let passing = grade >= 60; 
      output.innerHTML = `<span style="color: #f59e0b;">⚡ Evaluating Condition...</span><br>` +
                         `<code>let grade = ${grade};</code><br>` +
                         `<code>if (grade >= 60) {</code><br>` +
                         ` &nbsp;&nbsp;<span style="color: #4ade80;">▶ Output: "Student passes the module! [TRUE]"</span><br>` +
                         `<code>} else { ... }</code>`;
    } 
    else if (type === 'for') {
      output.innerHTML = `<span style="color: #c084fc;">⚡ Running Finite For Loop (Count 1 to 3)...</span><br>`;
      for(let i = 1; i <= 3; i++) {
        output.innerHTML += ` &nbsp;&nbsp;<span style="color: #e2e8f0;">Index [i] is now: <b>${i}</b></span><br>`;
      }
      output.innerHTML += `<span style="color: #a855f7;">✔ Loop terminating safely (i > 3).</span>`;
    } 
    else if (type === 'while') {
      output.innerHTML = `<span style="color: #34d399;">⚡ Running Conditional While Loop...</span><br>` +
                         `<code>while (isProcessing === true)</code><br>`;
      let count = 0;
      while(count < 2) {
        output.innerHTML += ` &nbsp;&nbsp;<span style="color: #94a3b8;">Processing iteration step ${count}...</span><br>`;
        count++;
      }
      output.innerHTML += `<span style="color: #10b981;">✔ Boolean flag flipped to false. Loop broken safely.</span>`;
    }
  }
</script>


