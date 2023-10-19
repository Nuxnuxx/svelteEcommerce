<script>
  import axios from 'axios'
  let email = ''
  let username = ''
  let password = ''
  let firstName = ''
  let lastName = ''

  const handlerSubmit = async (e) => {
    try {
      const response = await axios.post('https://fakestoreapi.com/users', {
          username: username,
          password: password,
          name: {
            firstname: firstName,
            lastname: lastName,
          },
          address: {
            city: 'kilcoole',
            street: '7835 new road',
            number: 3,
            zipcode: '12926-3874',
            geolocation: {
              lat: '-37.3159',
              long: '81.1496',
            },
          },
          phone: '1-570-236-7033',
      })
      console.log(response)
    } catch (e) {
      throw new Error(e)
    }
  }
</script>

<form class="form" action="" on:submit|preventDefault="{handlerSubmit}">
  <label for="email">Email :</label>
  <input placeholder="email" type="text" bind:value="{email}" />
  <label for="username">Username :</label>
  <input placeholder="username" type="text" bind:value="{username}" />
  <label for="password">Password :</label>
  <input placeholder="password" type="text" bind:value="{password}" />
  <div class="div">
    <label for="name">Name :</label>
    <input placeholder="name" type="text" bind:value="{firstName}" />
    <label for="lastname">Lastname :</label>
    <input placeholder="lastname" type="text" bind:value="{lastName}" />
  </div>
  <button>SUBMIT</button>
</form>

<style>
  .form {
    display: flex;
    flex-direction: column;
    align-items: center;
    row-gap: 3rem;
    padding: 2rem 0;
  }

  .div {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
		column-gap: 2rem;
  }

  input {
    width: 20%;
  }
</style>
