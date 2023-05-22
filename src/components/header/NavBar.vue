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
                <RouterLink to="/debit" class="transition">Debit Card</RouterLink>
                <RouterLink to="/credit" class="transition">Credit Card</RouterLink>
                <RouterLink to="/deposit" class="transition">Deposit</RouterLink>
                <RouterLink to="/e-sim" class="transition">eSIM</RouterLink>
            </nav>

            <div class="nav_bar__enter">
                <RouterLink to="/login" class="btn-enter transition">
                    <p>Enter</p>
                </RouterLink>
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
        display: flex;
        align-items: center;
        justify-content: space-between;
        color: rgba(255, 255, 255, 0.5);
        padding-bottom: 1%;

        @include large {
            font-size: 1.1rem;
        }
        @include medium {
            font-size: 0.8rem;
        }
        @include small {
            font-size: 0.5rem;
        }
        @include extra-small {
            font-size: 0.3rem;
        }
    }

    .nav-logo {

        .logo {
            background: no-repeat url(/src/assets/images/logo/logoWhite.svg);
            width: 6rem;
            height: 3rem;
            
            @include large {
                width: 10rem;
                height: 4rem;
            }
            @include medium {
                width: 5rem;
                height: 2rem;
            }
            @include small {
                width: 5rem;
                height: 2rem;
            }
        } 
    }
    .nav-bar {
        display: flex;
        align-items: center;
        
        .nav_bar__link {
            display: flex;

            a {
                margin-left: 2rem;
                transition: transform .4s cubic-bezier(0,0,.4,1);
                @include large {
                    margin-left: 5rem;
                }
                
                &:hover {
                    color: white;
                    transform: scale3d(1.15,1.15,1.15);
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

        @include large {
            margin-left: 5rem;
        }

        .btn-enter {
        border: 1px solid rgb(12, 24, 81);
        border-radius: 28px;
        padding: 7px 15px 7px 15px;
        text-decoration: none;

        @include large {
            padding: 10px 30px 10px 30px;
        }

        &:hover {
            color: white;
            border: 1px solid rgb(25, 48, 164);
        }
        }
    }
</style>
