<script>
</script>

<template>
    <div class="e-sim__description-container d-flex flex-column align-center pb-10">
    <div class="e-sim__description d-flex flex-row align-center bg-cl rounded-lg pl-10 pr-10 py-10 card-hover">
        <div>
            <h1 class="text-lg-h4 text-md-h5 text-sm-h6 pb-8">Install eSIM in 5 minutes</h1>
            <h2 class="text-lg-h5 text-md-subtitle-1 text-sm-subtitle-2 pl-5 pb-2">Don't wait for a courier - get an eSIM from AMC in 3 easy steps.</h2>
            <p class="text-lg-h6 text-md-subtitle-1 text-sm-subtitle-2">1. Download the AMC Bank application.</p>
            <p class="text-lg-h6 text-md-subtitle-1 text-sm-subtitle-2">2. Log in to the application - you can do this even if you are not an AMC subscriber.</p>
            <p class="text-lg-h6 text-md-subtitle-1 text-sm-subtitle-2">3. Go to the eSIM section and follow the instructions - you will be able to choose the number and tariff in the process.</p>
            <p class="text-lg-h6 text-md-subtitle-1 text-sm-subtitle-2">4. Ready! You will be able to register your new AMC eSIM right away.</p>
        </div>
        <div class="img-qr w-50 d-flex justify-center align-center">
            <span class="qr-icon">
                <img src="../../../public/images/icons/qr-code2.svg" alt="QR-code image">
            </span>
        </div>
    </div>
</div>
</template>

<style lang="scss">
.card-hover {
  transition: transform .4s cubic-bezier(0,0,.4,1);

  &:hover {
    transform: scale3d(1.04,1.04,1.04);
  }
}
.e-sim__description-container {
    width: 100%;
    .e-sim__description {
        width: 90%;

    @include small {
        flex-direction: column !important;
    }

    }
}
.qr-icon {
    width: 45%;
}
</style>