<template>
<div>
    <h1 class="htext">
        История Ferrari
    </h1>
    <p class="info">Ferrari - компания, выпускающая спортивные и гоночные автомобили. 
        Основана в 1947 году Энцо Феррари как Scuderia Ferrari, 
        компания спонсировала гонщиков и производила гоночные машины до 1947 года. 
        С 1947 года начала выпуск спортивных автомобилей, 
        разрешённых к использованию на дорогах общего пользования, под маркой «Ferrari S.p.A.». 
        На протяжении всей своей истории, компания участвует в различных гонках, особенно в Формуле-1, 
        где мы имеем наибольший успех. Эмблема «Феррари» — гарцующая лошадь на жёлтом фоне. 
        Традиционный цвет автомобилей — красный, но компания выпускает автомобили и других цветов.
    </p>

    <div class="card mb-3">
        <img src="@/static/fastest.jpg" class="card-img-top">
        <div class="card-body">
            <h5 class="card-title">Самая быстрая модель Ferrari - FERRARI LAFERRARI APERTA.</h5>
            <p class="card-text">
                В этом уникальном суперкаре Ferrari с открытым верхом незыблемые ценности итальянской марки подняты на совершенно новый уровень.
                Многочисленные исследования в области аэродинамики и успешный опыт в инженерии F1 и GT позволили конструкторам создать технологически идеальный кабриолет, 
                который способен подарить своему владельцу максимально яркие и самые захватывающие эмоции от вождения!</p>
                <div class="spec">
                    <div>
                        <img class="iconim2" src="@/static/engine.png"> 
                        <h5 class="card-title" id="st">Мощность</h5>
                        <p class="card-text" id="st2">963 Л/С</p>
                    </div>
                    <div>
                        <img class="iconim2" src="@/static/uskor.png"> 
                        <h5 class="card-title" id="st">0-200</h5>
                        <p class="card-text" id="st2"> меньше 7 сек.</p>
                    </div>
                    <div>
                        <img class="iconim2" src="@/static/speed.png">
                        <h5 class="card-title" id="st">Макс. скорость</h5> 
                        <p class="card-text" id="st2">350 км/ч</p>
                    </div>
                </div>
        </div>
    </div>

</div>
</template>
<style>
.info{
    color:white;
    text-align:center;
    margin-top:2vh;
    margin-bottom:2vh;
}
.iconim2{
    width: 18vh;
    text-align: center;
}
.spec{
    display:flex;
    justify-content: space-around;
    margin-top: 5vh;
}
#st{
    text-align: center;
    margin-top: 2vh;
}
#st2{
    text-align: center;
}
</style>