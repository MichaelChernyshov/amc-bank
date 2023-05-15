<template>
<header>
    <div class="navigation">
        <div class="nav-logo">
                <a href="/">
                    <div class="logo"></div>
                </a>
        </div>

        <div class="nav-bar">
            <nav class="nav_bar__link">
                <RouterLink to="/debit">Debit Card</RouterLink>
                <RouterLink to="/credit">Credit Card</RouterLink>
                <RouterLink to="/loans">Loans</RouterLink>
                <RouterLink to="/deposit">Deposit</RouterLink>
                <RouterLink to="/sim-card">Sim-Card</RouterLink>
            </nav>

            <div class="nav_bar__enter">
                <a href="/" class="btn-enter">
                    <p>Enter</p>
                </a>
            </div>
        </div>

        
        
    </div>
      

  </header>
        
</template>

<style lang="scss">
    .navigation {
        padding: 2%;
        display: flex;
        justify-content: space-between;
        color: white;
    }

    .nav-logo {

        .logo {
            background: no-repeat url(../assets/images/logo/logoWhite.svg);
            width: 80px;
            height: 30px;
        } 
    }
    .nav-bar {
        display: flex;
        align-items: center;
        
        .nav_bar__link {
            display: flex;

            a {
                margin-left: 2rem;
                font-size: 10px;

                &:first-child {
                    margin-left: 0;
                }
            }
        }
    }

    .nav_bar__enter {
        align-items: center;
        display: flex;
        margin-left: 2rem;

        .btn-enter {
        border: 1px solid rgb(12, 24, 81);
        border-radius: 28px;
        font-family: Arial;
        color: #ffffff;
        font-size: 10px;
        padding: 10px 20px 10px 20px;
        text-decoration: none;
        }
    }
</style>
