<template>
    <header :class="{change_color: scrollPosition > 600}">
        <div class="container p-4">
            <div class="logo">
                <a href="#" v-show="scrollPosition <= 600"><img height="30" src="../assets/images/light-logo.png" alt="Logo"></a>
                <a href="#" v-show="scrollPosition > 600"><img height="30" src="../assets/images/dark-logo.png" alt="Logo"></a>
            </div>
            <nav class="d-flex align-items-center">
                <ul class="d-flex">
                    <li v-for="link in menu" :key="link" class="ms-5">
                        <a href="#">{{link}}
                            <i class="fas fa-angle-down"></i>
                        </a>
                    </li>
                </ul>
                <div class="header-right ms-2">
                    <a href="#"><i class="fas fa-shopping-cart cart">
                        <div class="zero">0</div>
                    </i></a>
                    <a href="#" class="mx-4"><i class="far fa-user-circle"></i></a>
                    <input type="search" placeholder="Search...">
                    <button><i class="fas fa-search"></i></button>
                </div>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'SiteHeader',
    props: {
        menu: Array
    },
    data() {
        return {
            scrollPosition: null
        }
    },
    methods: {
        uptadeScroll() {
            this.scrollPosition = window.scrollY
        }
    },
    mounted() {
        window.addEventListener("scroll", this.uptadeScroll)
    }
}
</script>

<style lang="scss">
.change_color {
    background-color: white;
    box-shadow: 0px 0px 10px #a0a0a0;
    .zero {
        color: white !important;
        background-color: black !important;
    }
    a {
        color: #212529;
        &:hover {
            color: #41c457;
        }
    }
    input {
        background-color: #f5f5f5 !important;
    }
    button {
        background-color: #f5f5f5 !important;
        &:hover {
            background-color: #41c457 !important;
            color: white;
        }
    }
}
header {
    background-color: #1F2154;
    position: fixed;
    width: 100%;
    transition: 1s;
    z-index: 2;
    a {
        color: white;
        text-decoration: none;
        &:hover {
            color: white;
        }
    }
    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        ul {
            list-style: none;
            margin: 0;
            li {
                a {
                    display: flex;
                    align-items: center;
                    i {
                        font-size: 10px;
                        margin-left: 5px;
                    }
                }
            }
        }
        .cart {
            position: relative;
            .zero {
                position: absolute;
                top: -11px;
                right: -9px;
                color: black;
                height: 15px;
                width: 15px;
                background-color: white;
                border-radius: 50%;
                font-size: 10px;
                line-height: 15px;
                text-align: center;
            }
        }
        input {
            color: #696969;
            border: none;
            border-top-left-radius: 5px;
            border-bottom-left-radius: 5px;
            background-color: white;
            height: 48px;
            width: 50%;
            padding-left: 20px;
            &:focus-visible {
                outline: 0px solid transparent;
            }
        }
        button {
            border: none;
            background-color: white;
            color: #41c457;
            border-top-right-radius: 5px;
            border-bottom-right-radius: 5px;
            height: 48px;
            width: 48px;
            transition: 1s;
            &:hover {
                background-color: #41c457;
                color: white;
            }
        }
    }
}   
</style>