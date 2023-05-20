<script setup>
</script>

<template>
    <main class="debit__welcome-container">
    <article class="debit__welcome">
            <h1>Credit cards</h1>
            <p>Using credit card you can buy whatever you want with special offers</p>
        </article>
    </main>
</template>

<style lang="scss">
.debit__welcome-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100vw;
    height: 84vh;
}

.debit__welcome {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 70%;
    padding-bottom: 3%;
    
    
    h1 {
        font-size: 28px;
        font-weight: 300;
        word-spacing: 3px;
    }

    p {
        text-align: center;
        font-weight: 300;
        word-spacing: 2px;
    }
}
</style>