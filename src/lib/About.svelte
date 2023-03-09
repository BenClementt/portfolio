<script>
    import { onMount } from 'svelte';
</script>

<style>
.about__left{
    position: absolute;
    backdrop-filter: blur(10px);
    border-radius: 10px;
    padding: 2rem;
    height: 50%;
    width: 20%;
    margin-top: 10rem;
    margin-bottom: 10rem;
    left: 50px;
    text-align: left;
}

.about__left::after{
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to top, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.05));
    z-index: -1;
    border-radius: 10px;
    box-shadow: inset 0 0 0 1px rgb(255 255 255 / 10%), 0px 5px 20px 20px rgb(0 0 0 / 4%);
    overflow: hidden;
}

.about__left:hover::after{
    background: linear-gradient(to top, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.1));


}

.about__right{
    position: absolute;
    backdrop-filter: blur(10px);
    border-radius: 10px;
    padding: 2rem;
    height: 50%;
    width: 70%;
    margin-top: 10rem;
    margin-bottom: 10rem;
    right: 50px;
    text-align: left;
    background: linear-gradient(to top, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.05));
    box-shadow: inset 0 0 0 1px rgb(255 255 255 / 10%), 0px 5px 20px 20px rgb(0 0 0 / 4%);
}

@media screen and (max-width: 1158px){
    .about__right{
        display: none;
    }

    .about__left{
        width: 75%;
        margin-left: 0;
        margin-right: 0;
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
        font-size: 24px;
    }

}


</style>

<div class="about__left">
    <h3 class="about__title">
        <span class="greeting">Hey,</span> <br>
        <span class="name animate__animated animate__zoomIn animate__slow animate__delay-1s">I'm Ben Clement</span>    
    </h3>
    <div class="about__info mt-4 animate__animated animate__fadeInUp animate__slow animate__delay-2s">
        <p class="about__text">
            I'm a freelance lighting designer and multi-skilled technician based in London, England.
        </p>

        <p class="about__text mt-4">
            I have a passion for Technology and the Arts, and I'm always looking for new opportunities to learn and grow.
        </p>
    </div>
</div>

<div class="about__right">
    Some content here eventually!
</div>
