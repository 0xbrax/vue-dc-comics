<template>
    <footer>
        <div class="upper-footer">
            <div class="container flex just-sp-bt align-ctr up-case">
                <div v-for="(special, specialIndex) in specialLinks" :key="specialIndex">
                    <a :href="special.url" class="flex align-ctr">
                        <img :src="special.icon" :alt="special.name">
                        <div class="ml-10">{{special.name}}</div>
                    </a>
                </div>
            </div>
        </div>

        <div class="middle-footer">
            <div class="container flex">
                <div class="flex wrap">
                    <div class="link-list">
                        <div>
                            <h3 class="up-case">DC Comics</h3>
                            <ul>
                                <li class="mt-2" v-for="(link, linkIndex) in navLinks" :key="linkIndex">
                                    <a :href="link.url" :class="link.active?'active':''" >
                                        {{link.text}}
                                    </a>
                                </li>
                            </ul>
                        </div>

                        <div class="mt-25">
                            <h3 class="up-case">Shop</h3>
                            <ul>
                                <li class="mt-2" v-for="(link, linkIndex) in shopLinks" :key="linkIndex">
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
                            <li class="mt-2" v-for="(link, linkIndex) in mainLinks" :key="linkIndex">
                                <a :href="link.url" :class="link.active?'active':''" >
                                    {{link.text}}
                                </a>
                            </li>
                        </ul>
                    </div>
                    
                    <div class="link-list">
                        <h3 class="up-case">Sites</h3>
                        <ul>
                            <li class="mt-2" v-for="(link, linkIndex) in infoLinks" :key="linkIndex">
                                <a :href="link.url" :class="link.active?'active':''" >
                                    {{link.text}}
                                </a>
                            </li>
                        </ul>
                    </div>
                    
                </div>
            </div>
        </div>

        <div class="bottom-footer">
            <div class="container up-case flex just-sp-bt align-ctr">
                <div>
                    <a class="button main-btn" href="#">
                        Sign-up now!
                    </a>
                </div>

                <div class="flex align-ctr">
                    <h4 class="follow-us">
                        Follow us
                    </h4>
                    <div class="ml-10" v-for="(social, socialIndex) in socialLinks" :key="socialIndex">
                        <a :href="social.url">
                            <img :src="social.icon" :alt="social.site">
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'DcFooter',
    data() {
        return {
            specialLinks: [
                {
                    name: 'Digital comics',
                    icon: require('@/assets/img/buy-comics-digital-comics.png'),
                    url: '#'
                },
                {
                    name: 'DC merchandise',
                    icon: require('@/assets/img/buy-comics-merchandise.png'),
                    url: '#'
                },
                {
                    name: 'Subscription',
                    icon: require('@/assets/img/buy-comics-subscriptions.png'),
                    url: '#'
                },
                {
                    name: 'Comic shop locator',
                    icon: require('@/assets/img/buy-comics-shop-locator.png'),
                    url: '#'
                },
                {
                    name: 'DC power visa',
                    icon: require('@/assets/img/buy-dc-power-visa.svg'),
                    url: '#'
                }
            ],
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
            ],
            socialLinks: [
                {
                    site: 'facebook',
                    icon: require('@/assets/img/footer-facebook.png'),
                    url: '#'
                },
                {
                    site: 'twitter',
                    icon: require('@/assets/img/footer-twitter.png'),
                    url: '#'
                },
                {
                    site: 'youtube',
                    icon: require('@/assets/img/footer-youtube.png'),
                    url: '#'
                },
                {
                    site: 'pinterest',
                    icon: require('@/assets/img/footer-pinterest.png'),
                    url: '#'
                },
                {
                    site: 'periscope',
                    icon: require('@/assets/img/footer-periscope.png'),
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/common.scss';
    @import '../style/utility.scss';


    footer {
        color: #ffffff;
    }

    .upper-footer {
        background-color: $brand-color;
        padding: 50px 0;
    }

    .upper-footer {
        img {
            height: 50px;
        }
        .container div:last-of-type img {
            height: 35px;
        }
        a {
            color: #ffffff;
        }
    }

    .middle-footer {
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
    }

    .middle-footer {
        .container {
            background-image: url('../assets/img/dc-logo-bg.png');
            background-repeat: no-repeat;
            background-position: right;
            padding: 25px 0;
        }
    }

    .link-list {
        width: calc(100% / 3);
    }

    ul {
        a {
            color: $grey-light;
            &:hover {
                color: #ffffff;
            }
        }
    }

    .bottom-footer {
        height: 100px;
        background-color: $grey-dark;
    }

    .bottom-footer {
        .container {
            height: 100%;
        }
        .button:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }
    }

    .follow-us {
        color: $brand-color;
    }
</style>