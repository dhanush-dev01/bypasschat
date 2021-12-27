<script>
  import { username, user } from './user';

  function signout() {
    user.leave();
    username.set('');
  }
</script>

<header>
<img src="/logo.jpeg" alt="logo"/>
<span>bypass chat</span>
  {#if $username}
    <div class="user-bio">
      
      <span>Hello <strong>{$username}</strong></span>
      <img src={`https://avatars.dicebear.com/api/initials/${$username}.svg`} alt="avatar" /> 
    </div>

    <button class="signout-button" on:click={signout}>Sign Out</button>

    {:else}
        <h4>join the chat now</h4>
  {/if}
</header>