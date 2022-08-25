<template>
    <header>
        <div class="container flex just-sp-bt align-ctr">
            <a href="#">
            <img src="@/assets/img/dc-logo.png" alt="DC Comics">
        </a>

        <ul class="up-case">
            <li v-for="(link, linkIndex) in links" :key="linkIndex">
                <a :href="link.url" :class="link.active?'active':''" >
                    {{link.text}}
                </a>
            </li>
        </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: 'DcHeader',
    data() {
        return {
            links: [
                {
                    text: 'characters',
                    url: '#',
                    active: false
                },
                {
                    text: 'comics',
                    url: '#',
                    active: true
                },
                {
                    text: 'movies',
                    url: '#',
                    active: false
                },
                {
                    text: 'TV',
                    url: '#',
                    active: false
                },
                {
                    text: 'games',
                    url: '#',
                    active: false
                },
                {
                    text: 'collectibles',
                    url: '#',
                    active: false
                },
                {
                    text: 'videos',
                    url: '#',
                    active: false
                },
                {
                    text: 'fans',
                    url: '#',
                    active: false
                },
                {
                    text: 'news',
                    url: '#',
                    active: false
                },
                {
                    text: 'shop',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/common.scss';


    header {
        height: 80px;
        color: $black-variant;
    }

    header {
        img {
            height: 60px;
        }
    }

    ul {
        li, a {
            display: inline-block;
        }
    }

    ul {
        li {
            a {
                padding: 0 10px;
                line-height: 80px;
                color: $black-variant;

                &.active, &:hover {
                    color: $brand-color;
                    box-shadow: inset 0px -5px 0px 0px $brand-color;
                }
            }
        }
    }


</style>