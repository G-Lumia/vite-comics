<template>
    <div class="card col-12 col-sm-6 col-md-4 col-lg-3 col-xl-2">
        <div class="card-body">
            <div class="thumb p-3">
                <img class="cropped" :src="thumb" :alt="series">
            </div>
            <h2 class="py-4 text-light text-center">
                {{ series }}
            </h2>
        </div>
    </div>
</template>
<script>
export default {
    name : 'comics',
    props : ['thumb' , 'price' , 'series' , 'type']
}
</script>

<style lang="scss" scoped>
    .cropped{
        height: 300px;
        width: 300px;
        object-fit: cover;
        object-position:top;
    }
    .thumb{
        width: 300px;
        height: 300px;
    }

    .card{
        background-color: transparent;
        width: 400px;
    }
</style>