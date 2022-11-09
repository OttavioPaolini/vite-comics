<script>
export default{
    name: "AppHeader",
    data(){
        return{
            links:[
                {
                    name: "CHARACTERS",
                    href: "/characters",
                    active: false
                },
                {
                    name: "COMICS",
                    href: "/comics",
                    active: true,
                },
                {
                    name: "MOVIES",
                    href: "/movies",
                    active: false
                },
                {
                    name: "TV",
                    href: "/tv",
                    active: false
                },
                {
                    name: "GAMES",
                    href: "/games",
                    active: false
                },
                {
                    name: "COLLECTIBLES",
                    href: "collectibles",
                    active: false
                },
                {
                    name: "VIDEO",
                    href: "video",
                    active: false
                },
                {
                    name: "FANS",
                    href: "fans",
                    active: false
                },
                {
                    name: "NEWS",
                    href: "news",
                    active: false
                },
                {
                    name: "SHOP",
                    href: "shop",
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
                display: inline-block;
                border-bottom: 3px solid blue;
            }
        }
    }

</style>