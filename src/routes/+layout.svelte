<nav class="navbar">
    <div>
    <img src="ansible-certification-exams.png" style="width: 3em; padding-top: 1em;" alt="logo">    
    </div>

    <div>   
        <a href="/">Home</a>
        <a href="/dashboard">Dashboard</a>
        <a href="/settings">Settings</a>
    </div>
 
  </nav>
  
  <slot></slot>

  <style>
    .navbar{
        display: flex;
        justify-content: space-around;
        align-items: center;
        margin: auto;
        max-width: 80em;
        padding-top: 1em;
    }

    .navbar a {
        padding: 1em;
    }
  </style>