<script>
export default{
    name: "AppHeader",
    data(){
        return{
            links:[
                {
                    name: "CHARACTERS",
                    href: "",
                    active: false
                },
                {
                    name: "COMICS",
                    href: "",
                    active: false,
                },
                {
                    name: "MOVIES",
                    href: "",
                    active: false
                },
                {
                    name: "TV",
                    href: "",
                    active: false
                },
                {
                    name: "GAMES",
                    href: "",
                    active: false
                },
                {
                    name: "COLLECTIBLES",
                    href: "",
                    active: false
                },
                {
                    name: "VIDEO",
                    href: "",
                    active: false
                },
                {
                    name: "FANS",
                    href: "",
                    active: false
                },
                {
                    name: "NEWS",
                    href: "",
                    active: false
                },
                {
                    name: "SHOP",
                    href: "",
                    active: false
                },
            ]
        }
    }
}
</script>
<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC comics logo">
            </div>
            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :class="{'active': link.active}" :href="link.href">{{link.name}}</a>       
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/mixin" as *;

header{
    background-color: white;
}
    .container{
        @include flex-center();
        justify-content: space-between;
    }
        ul{
            line-height: 140px;
            @include flex-center();
            
        }
            li{
                margin-left: 1.5rem;
            }
            a {
                    &:hover,
                    &.active {
                        height: 140px;
                        border-bottom: 3px solid blue;
                    }
                }

</style>