<template>
    <ul class="sidenav app-sidenav" :class="{open: value}">

        <li v-for="(iink,index) in links" :key="index + iink.url">
            <router-link active-class="active" exact :to="iink.url" class="waves-effect waves-orange pointer">
                {{iink.title}}
            </router-link>
        </li>

    </ul>
</template>

<style lang="scss">
    .sidenav{
        li{
            .active{
                background-color: #f2f2f2;
            }
        }
    }
</style>

<script>
export default {
    props:['value'],
    data: () =>({
        links:[
            {
                title:'Счет',
                url:'/'
            },

            {
                title:'История',
                url:'/history'
            },

            {
                title:'Планирование',
                url:'/planning'
            },

            {
                title:'Новая запись',
                url:'/record'
            },

            {
                title:'Категории',
                url:'/categories'
            }
        ]
    })
}
</script>
