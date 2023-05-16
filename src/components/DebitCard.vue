<script>
export default {
    data() {
        return {
            isBtnPopCloseFocused: false
        }
    },
    methods: {
        toggleToItemEditForm() {
        console.log(this.$refs.editButton);
        this.isEditing = true;
        }
    }
}
</script>

<template>
    <main>
        <article>
            <h1 class="debit__welcome">Debit cards</h1>
            <p>Using debit card is the best way to pay for everything you want and after all - receive a cashback.</p>
        </article>

        <section>
            <div class="debit__buttons">
                <button type="button" class="button" ref="normButton" @click="toggleToItemEditForm">Normal</button>
                <button type="button" class="button" ref="premButton" @click="toggleToItemEditForm">Premium</button>
            </div>
        </section>
    </main>

</template>

<style lang="scss">

.debit__buttons {
    display: flex;
    justify-content: space-around;
    background-color: grey;
    width: 30%;
    height: 20px;

    .button:focus {
        background-color: red;
    }
}
</style>