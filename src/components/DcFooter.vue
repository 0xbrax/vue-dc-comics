<template>
    <footer>
        <div class="upper-footer">
            <div class="container">

            </div>
        </div>

        <div class="middle-footer">
            <div class="container flex">
                <div class="flex wrap">
                    <div class="link-list">
                        <div>
                            <h3 class="up-case">DC Comics</h3>
                            <ul>
                                <li v-for="(link, linkIndex) in navLinks" :key="linkIndex">
                                    <a :href="link.url" :class="link.active?'active':''" >
                                        {{link.text}}
                                    </a>
                                </li>
                            </ul>
                        </div>

                        <div>
                            <h3 class="up-case">Shop</h3>
                            <ul>
                                <li v-for="(link, linkIndex) in shopLinks" :key="linkIndex">
                                    <a :href="link.url" :class="link.active?'active':''" >
                                        {{link.text}}
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div class="link-list">
                        <h3 class="up-case">DC</h3>
                        <ul>
                            <li v-for="(link, linkIndex) in mainLinks" :key="linkIndex">
                                <a :href="link.url" :class="link.active?'active':''" >
                                    {{link.text}}
                                </a>
                            </li>
                        </ul>
                    </div>
                    
                    <div class="link-list">
                        <h3 class="up-case">Sites</h3>
                        <ul>
                            <li v-for="(link, linkIndex) in infoLinks" :key="linkIndex">
                                <a :href="link.url" :class="link.active?'active':''" >
                                    {{link.text}}
                                </a>
                            </li>
                        </ul>
                    </div>
                    
                </div>

                <div>

                </div>
            </div>
        </div>

        <div class="bottom-footer">
            <div class="container">

            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'DcFooter',
    data() {
        return {
            navLinks: [
                {
                    text: 'Characters',
                    url: '#'
                },
                {
                    text: 'Comics',
                    url: '#'
                },
                {
                    text: 'Movies',
                    url: '#'
                },
                {
                    text: 'TV',
                    url: '#'
                },
                {
                    text: 'Games',
                    url: '#'
                },
                {
                    text: 'Videos',
                    url: '#'
                },
                {
                    text: 'News',
                    url: '#'
                }
            ],
            mainLinks: [
                {
                    text: 'Term Of Use',
                    url: '#'
                },
                {
                    text: 'Privacy policy (New)',
                    url: '#'
                },
                {
                    text: 'Ad Choices',
                    url: '#'
                },
                {
                    text: 'Advertising',
                    url: '#'
                },
                {
                    text: 'Jobs',
                    url: '#'
                },
                {
                    text: 'Subscriptions',
                    url: '#'
                },
                {
                    text: 'Talent Workshops',
                    url: '#'
                },
                {
                    text: 'CPSC Certificates',
                    url: '#'
                },
                {
                    text: 'Ratings',
                    url: '#'
                },
                {
                    text: 'Shop Help',
                    url: '#'
                },
                {
                    text: 'Contact Us',
                    url: '#'
                }
            ],
            infoLinks: [
                {
                    text: 'DC',
                    url: '#'
                },
                {
                    text: 'MAD Magazine',
                    url: '#'
                },
                {
                    text: 'DC Kids',
                    url: '#'
                },
                {
                    text: 'DC Universe',
                    url: '#'
                },
                {
                    text: 'DC Power Visa',
                    url: '#'
                }
            ],
            shopLinks: [
                {
                    text: 'Shop DC',
                    url: '#'
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/common.scss';


    footer {
        color: #ffffff;
    }

    .upper-footer {
        height: 100px;
        background-color: $brand-color;
    }

    .middle-footer {
        background-image: url('../img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
    }

    .link-list {
        width: calc(100% / 3);
    }

    ul {
        a {
            color: $grey-light;
        }
    }

    .bottom-footer {
        height: 100px;
        background-color: $grey-dark;
    }
</style>