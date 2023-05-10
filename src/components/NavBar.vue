<template><header>
    <div class="nav-bar">
      <nav>
        <a href="/">
                <div class="logo"></div>
        </a>
        <RouterLink to="/debit">Debit Card</RouterLink>
        <RouterLink to="/credit">Credit Card</RouterLink>
        <RouterLink to="/loans">Loans</RouterLink>
        <RouterLink to="/deposit">Deposit</RouterLink>
        <RouterLink to="/sim-card">Sim-Card</RouterLink>
        <RouterLink to="/login">Login</RouterLink>
      </nav>
    </div>
  </header>
        
</template>

<style lang="scss">
    img {
        max-width: 5rem;
    }

    .logo {
        background:no-repeat url(../assets/images/logo/logoBlack.svg);
        width: 100px;
        height: 30px;
    }    
    .nav-bar {
        margin: 2%;
    }
    nav {
        display: flex;
        justify-content: space-between;
    }
</style>
