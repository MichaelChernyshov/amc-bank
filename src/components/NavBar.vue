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
                <RouterLink to="/e-sim">eSIM</RouterLink>
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
    header {
        padding: 2%;
    }
    .navigation {
        font-size: 8px;
        display: flex;
        justify-content: space-between;
        color: rgba(255, 255, 255, 0.5);
        padding-bottom: 1%;
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
                
                &:hover {
                    color: white;
                }

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
        padding: 7px 15px 7px 15px;
        text-decoration: none;

        &:hover {
            color: white;
            border: 1px solid rgb(25, 48, 164);
        }
        }
    }
</style>
