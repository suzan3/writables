<template>
<q-page class="bg px-10 q-pt-xl">
    <div class="row">
        <div class="col-12 text-center">
            <p class="title"> SERVICES </p>
        </div>
    </div>
    <div class="row">
        <div class="col-md-6 col-12 q-mt-xl">
            <q-card class="my-card shadow-10">
                <q-card-section class="bg-primary text-center text-white q-py-lg">
                    <div class="text-h6">Writer</div>
                </q-card-section>

                <q-separator />

                <q-card-actions class="no-p" align="center">
                    <q-list separator class="w-100">
                        <q-item class="first" v-for='index in ListOfWriters' :key='index'  clickable v-ripple>
                            <q-item-section>{{index.name}}</q-item-section>
                            <q-item-section side>{{index.price}}</q-item-section>
                        </q-item>
                    </q-list>
                </q-card-actions>
            </q-card>
        </div>
        <div class="col-md-6 col-12 q-mt-xl">
            <q-card class="my-card shadow-10">
                <q-card-section class="bg-primary text-center text-white q-py-lg">
                    <div class="text-h6">Entity</div>
                </q-card-section>

                <q-separator />

                <q-card-actions class="no-p" align="center">
                    <q-list separator class="w-100">
                        <q-item v-for='index in ListOfEntity' :key='index'  clickable v-ripple>
                            <q-item-section>{{index.name}}</q-item-section>
                            <q-item-section side>{{index.price}}</q-item-section>
                        </q-item>
                    </q-list>
                </q-card-actions>
            </q-card>
        </div>
        <div class="col-md-6 col-12 q-mx-auto q-mt-xl">
            <q-card class="my-card shadow-10">
                <q-card-section class="bg-primary text-center text-white q-py-lg">
                    <div class="text-h6">Talent</div>
                </q-card-section>

                <q-separator />

                <q-card-actions class="text-center q-pa-xl talent" align="center">
                    UPLOAD YOUR TALENT REEL TO ENROLL IN WRITABLES’ TALENT DATABASE
                    <br> <br>
                    FREE OF CHARGE
                </q-card-actions>
            </q-card>
        </div>
    </div>
</q-page>
</template>

<style>
.first:nth-child(1){
    color: #0392FF;
    text-decoration: underline;

}
.q-item{
    min-height: auto !important;
    padding-bottom: 2px;
    padding-top: 2px;
    padding-left: 10px;
    padding-right: 10px;
    font-family: 'HelveticaNeueLTStd-Roman';
    font-size: 15px;
}
.q-card > div:not(:first-child){
    padding-bottom: 20px;
    padding-top: 15px;
}
.q-card{
    width: 85%;
    margin: auto;
    border-radius: 1rem;
}
.q-item:nth-child(odd){
background-color: #C7C9CB !important;
}
.text-h6{
    font-family: 'AGENCYR';
    font-size: 54px;
}
.q-list--separator > .q-item-type + .q-item-type{
    border: none !important;
}
.q-item__section--side{
    color: black !important;
}
.bg-primary {
    background-color: #BC8037 !important;
}
.w-100{
    width: 100% !important;
}
.no-p{
    padding-left: 0 !important;
    padding-right: 0 !important;
     
}
.talent{
    font-family: 'HelveticaNeueLTStd-Roman';
    font-size: 15px;
}
</style>

<script>
const writers = [
    {
        name:'Submit Project',
        price:''
    },
    {
        name : 'SERIES',
        price : '49$'
    },
    {
        name : 'MOVIES',
        price : '49$'
    },
    {
        name : 'PLAYS',
        price : '49$'
    },
    {
        name : 'BOOKS',
        price : '49$'
    },
    {
        name : 'STORIES',
        price : '49$'
    },
    {
        name : 'POEMS',
        price : '15$'
    },
    {
        name : 'SONGS',
        price : '9$'
    },
    {
        name : 'GAMES',
        price : '25$'
    },
    {
        name : 'INTELLECTUAL PROPERTY',
        price : '275$'
    },
    {
        name : 'PROOFREADING/ TREATMENT',
        price : 'REQUEST QUOTATION'
    },
   

];
const entity = [
    {
        name : 'PLATFORM ACCESS',
        price : ''
    },
    {
        name : 'SERIES',
        price : '2450$'
    },
    {
        name : 'MOVIES',
        price : '2450$'
    },
    {
        name : 'PLAYS',
        price : '1950$'
    },
    {
        name : 'BOOKS',
        price : '450$'
    },
    {
        name : 'STORIES',
        price : '450$'
    },
    {
        name : 'POEMS',
        price : '950$'
    },
    {
        name : 'SONGS',
        price : '450$'
    },
    {
        name : 'GAMES',
        price : '1950$'
    },
    {
        name : 'TALENTS',
        price : 'FREE OF CHARGE'
    },
    {
        name : 'SHORTLISTING',
        price : 'FREE OF CHARGE'
    },
   

];
export default {
    name: 'services',
     data() {
        return {
            ListOfWriters: writers,
            ListOfEntity: entity,
        }
    }
}
</script>
