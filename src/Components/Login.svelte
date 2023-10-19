<script>
 import axios from 'axios' 
 let username = ''
 let password = ''
 
 //user test
 //username johnd
 //password m38rmF$

 const handlerSubmit = async () => {
    
    try {
      const response = await axios.post('https://fakestoreapi.com/auth/login', {
        username: username,
        password: password,
      })
      console.log(response)
    } catch (e) {
      throw new Error(e)
    }
  }
</script>




<form class="form" action="" on:submit|preventDefault="{handlerSubmit}">
    <label for="username">Username :</label>
    <input placeholder="username" type="text" bind:value="{username}" />
    <label for="password">Password :</label>
    <input placeholder="password" type="text" bind:value="{password}" />
    <button>SUBMIT</button>
</form>



<!--<div>
	<form action=""> 
    <label for="username">Username :</label>
    <input placeholder="name" type="text" bind:value="{username}" />
    <label for="password">Password :</label>
    <input placeholder="password" type="text" bind:value="{password}" />
    <button type="submit" on:click="{handlerSubmit}">Se connecter</button>
	</form>
</div>
-->




<style>
    .form {
      display: flex;
      flex-direction: column;
      align-items: center;
      row-gap: 3rem;
      padding: 2rem 0;
    }
  
    input {
      width: 20%;
    }
 </style>
  