
<div class="container">

    <h1>Super coole Ansible UI by Thommy</h1>
    <form on:submit={handleSubmit} style="width: 100%;">

        <div>
            <label for="username">Username:</label>
            <input type="text" id="username" bind:value={username} required />
        </div>

        <div>
            <label for="password">Password:</label>
            <input type="password" id="password" bind:value={password} required />
        </div>

        <div>
          <label for="submit_buttom" style="color: red;">{wrongPw}</label>
            <button name="submit_button" type="submit">Login</button>
        </div>

    </form>

</div>

<script>
    let username = "";
    let password = "";
    let wrongPw = "";

    async function handleSubmit(event) {
      event.preventDefault();
  
      const response = await fetch("http://127.0.0.1:21234/login", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
        },
        body: JSON.stringify({ username, password }),
      });
  
      const data = await response.json();
  
      if (response.ok) {
        console.log("Authenticated successfully:", data);
      } else {
        wrongPw = "wrong password";
        console.log("Authentication failed:", data);
      }
    }
  </script>

<style>
    
    .container{
        height: 100vmin;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    form{
        max-width: 30em;
    }

</style>