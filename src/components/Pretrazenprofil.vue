<template>
    <div class="pretrazenprofil">
        <div class="card">
            <h1>{{podatak.ime}} {{podatak.prezime}}</h1>
            <p>{{podatak.spol}}</p>
            <p>{{podatak.brojgodina}}</p>
            <p>{{podatak.grad}}</p>
            <p>{{podatak.kontakt}}</p>
            <p>{{podatak.ostalo}}</p>
        </div>
    </div>
</template>


<script>
import store from '@/store.js'
export default {
    props: ["podatak"]
}
</script>

<style scoped>

</style>
