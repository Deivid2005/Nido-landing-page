<template>
    <section class="contenido d-flex flex-column " style="min-height: 650px; position: relative; padding: 40px; background: linear-gradient(180deg,  #030B33 60%, #0022A6 100%); ">
        <h2 class="tituloPowerstartup">
            Power-ups para<br>tu Startup
        </h2>
        <div class="powerups-labels">
            <span class="label label1">
                Acesso a la comunidad

            </span>
            <span class="label label2">
                Acceso al programa de beneficios
            </span>
            <span class="label label3">
                networking 
            </span>
            <span class="label label4">
                Acesso a Co-Working
            </span>
            <span class="label label5">
                Acompañamiento
            </span>
            <span class="label label6">
                Red de inversionistas
            </span>
        </div>
    
        <img src="../assets/estructura.png" alt="" style="position: absolute ; left:60px; bottom: 40px; width: 250px;">
        <img src="../assets/estrella.png" alt="" style="position: absolute; width: 250px; right: 0px; top:200px;">
    </section>
</template>
<style>
.tituloPowerstartup{
    color: #cfc3f7;
    font-size: 50px;
    font-weight: 700;
    text-align: left;
    margin: 40px 0 0 60px;
    
}
.powerups-labels {
    position: absolute;
    top: 180px;
    left: 0;
    width: 100%;
    height: 100px;
    padding-block: 200px;
}
.label {
    position:absolute;
    background: #e7e6fb;
    color: #030B33;
    font-size: 1.25rem;
    font-weight: 600;
    padding: 12px 28px;
    border-radius: 10px;
    box-shadow: 0 2px 12px 0 rgba(0,0,0,0.08);
}
.label1 { top: 90px; left: 120px; transform: rotate(-8deg);}
.label2 { top: 90px; right: 380px; transform: rotate(3deg);}
.label3 { top: -40px; right: 160px; transform: rotate(8deg);}
.label4 { top: 200px; left: 360px; transform: rotate(5deg);}
.label5 { top: 360px; left: 620px; transform: rotate(-3deg);}
.label6 { top: 290px; right: 150px; transform: rotate(2deg);}
</style>
