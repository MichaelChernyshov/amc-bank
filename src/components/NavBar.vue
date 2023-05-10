<template>
<header>
    <div class="nav-bar">
        <div>
            <span>
                <a href="/">
                    <div class="logo"></div>
                </a>
            </span>
        </div>

        <div>
            <nav>
                <RouterLink to="/debit">Debit Card</RouterLink>
                <RouterLink to="/credit">Credit Card</RouterLink>
                <RouterLink to="/loans">Loans</RouterLink>
                <RouterLink to="/deposit">Deposit</RouterLink>
                <RouterLink to="/sim-card">Sim-Card</RouterLink>
            </nav>
        </div>

        <div>
            <span>
                <a href="/">
                    <div class=""></div>
                </a>
            </span>
        </div>
        
    </div>
      

  </header>
        
</template>

<style lang="scss">
    .logo {
        max-width: 5rem;
        background: no-repeat url(../assets/images/logo/logoBlack.svg);
        width: 100px;
        height: 30px;
    }    
    .nav-bar {
        margin: 2%;
        display: flex;
        justify-content: space-between;
    }
    .nav-div {
        display: flex;
    }
</style>
