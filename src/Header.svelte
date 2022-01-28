<script>
  import { username, user } from "./user";

  function signout() {
    user.leave();
    username.set("");
  }
</script>

<header>
  <img src="./../computer.svg.png" alt="LOGO" />
  {#if $username}
    <div class="user-bio">
      <span>Hello <strong>{$username}</strong></span>
      <img
        src={`https://avatars.dicebear.com/api/initials/${$username}.svg`}
        alt="avatar"
      />
    </div>

    <button class="signout-button" on:click={signout}>Sign Out</button>
  {:else}
    <h3>BCA Chat</h3>
  {/if}
</header>
