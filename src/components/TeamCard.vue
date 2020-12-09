<template>
    <section>
        <a name="team"></a>
        <div class="card text-white bg-dark">
            <div class="d-flex justify-content-center p-2">
                <img :src="member.image" alt="..." width="210px" height="260px"> 
            </div>
            <div class="card-body">
                <h5 class="card-title">{{member.nombre}}</h5>
                    <p class="card-text">{{member.descripcion}}</p>
                    <p class="card-text">{{member.rol}}</p>
                    
                    <button type="button" class="btn btn-primary">LINKEDIN</button><br>
                    <button type="button" class="btn btn-secondary">GITHUB</button>
            </div>
        </div>
    </section>   
</template>

<script>

    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
