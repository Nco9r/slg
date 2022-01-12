<template>
<section class="story">
    <div class="story_block">

    <div class="block_left">
        <h2><span class="yellow">SLGrealisation</span> propose ses service de la maison à la piscine.</h2>
        <h3>L'entreprise marche en famille</h3>
    </div>
    <div class="block_right">
        <p>Nous sommes en mesure de répondre à tous vos besoins en matière de création de piscine de A à Z, de maçonnerie générale ou de terrassement. N’hésitez pas à nous contacter. Intervention possible sur Bordeaux Métropole et dans sa région.</p>
    </div>
    </div>
</section>
  
</template>

<script>
export default {

}
</script>

<style scoped>

/* VARIABLES */

.yellow {
    color: var(--yellow);
}

/* PAGE */

.story {
    background: var(--background-gradient);

    margin-top: -110px;
    padding: 0px 10Px 30px 26px;

}

.block_left {
    padding-top: 160px;
}

.block_left h2 {
    font-size: 22Px;
    color: var(--bleu);
    line-height: 32px;
}

.block_left h3 {
    font-size: 18Px;
    color: var(--bleu);
    margin-top: 30px;
    margin-bottom: 30px;
}

.block_right p {
    color: var(--bleu);
    line-height: 28px;
}

@media screen and (min-width: 1024px) {
    .story_block {
        display: flex;
        padding-top: 150px;
        max-width: 900px;
        margin: auto;
        justify-content: space-between;
     
    }

    .block_left {
        width: 45%;
        padding-top: 100px;
    }

     .block_right {
        width: 50%;
        margin-top: 132px;
    }


.block_left h3 {
    font-size: 20Px;
    color: var(--bleu);
    margin-top: 30px;
    margin-bottom: 30px;

}
.block_left h2 {
    font-size: 26Px;
    color: var(--bleu);
    line-height: 36px;
}
    .block_right p {
        font-size: 15px;
        
    }
}



</style>