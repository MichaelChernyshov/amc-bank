<script></script>

<template>
<div class="d-flex flex-column align-center pb-10">
    <div class="d-flex flex-row align-center bg-cl rounded-s-xl pl-10 pr-10 py-10">
        <div class="d-flex justify-center align-center pr-11">
            <span class="pr-10">
                <img src="../../../public/images/icons/deposit/safe.svg" class="qq">
            </span>
        </div>
        <div class="w-75">
            <p class="text-lg-h4 text-md-h5 text-sm-h6">Deposit "AMC"</p>
            <p class="text-lg-h6 text-md-subtitle-1 text-sm-subtitle-2">Best choice for everyone</p>
            <v-chip-group>
                <v-chip>Good %</v-chip> <v-chip>Without taxes</v-chip> <v-chip>Without fees</v-chip>
            </v-chip-group>
            <div class="desc-dep d-flex flex-row">
                <p>up to 5.0%</p>
                <p>from 500 euro</p>
                <p>from 1 month</p>
            </div>
        </div>
    </div>
</div>
</template>

<style lang="scss">
.desc-dep {
    p {
        padding-right: 15%;
        &:last-child {
            padding-right: 0;
        }
    }
}
.qq {
    width: 100px;
    height: 100px;
}
</style>