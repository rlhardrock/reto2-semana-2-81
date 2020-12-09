<template>
    <div>
    
      <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators"> 
            <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
            <li data-target="#carouselExampleCaptions" data-slide-to="1" class=""></li> 
            <li data-target="#carouselExampleCaptions" data-slide-to="2" class=""></li> 
        </ol>
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="@/assets/img/BigData.jpeg" alt="Data science" class="bd-placeholder-img bd-placeholder-img-lg d-block w-100"  height="550">

                    <div class="carousel-caption d-none d-md-block"> 
                        <h3>Data Science</h3>
                
                    </div>
            </div>
            <div class="carousel-item">
                <img src="@/assets/img/DataScience.jpeg" alt="Big data" class="bd-placeholder-img bd-placeholder-img-lg d-block w-100"  height="550">
                
                    <div class="carousel-caption d-none d-md-block"> 
                        <h3>Big Data</h3> 
                        
                    </div> 
            </div>
            <div class="carousel-item"> 
                <img src="@/assets/img/MachineLearning.jpeg" alt="Big data" class="bd-placeholder-img bd-placeholder-img-lg d-block w-100"  height="550">
                    
                    <div class="carousel-caption d-none d-md-block"> 
                        <h3>Machine Learning</h3> 
                            
                    </div> 
            </div>  
        </div>

        <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev"> 
            <span class="carousel-control-prev-icon" aria-hidden="true"></span> 
            <span class="sr-only">Back</span> 
        </a> 
        <a class="carousel-control-next" href="#carouselExampleCaptions" role="button"
        data-slide="next"> 
            <span class="carousel-control-next-icon" aria-hidden="true"></span> 
            <span class="sr-only">Next</span> 
        </a> 
    </div>  

    </div>
</template>

<script>

export default {
    name: "SeccionBanner"
}
</script>

<style scoped>

</style>