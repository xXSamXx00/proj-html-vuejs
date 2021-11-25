<template>
    <header>
        <div class="container p-4">
            <div class="logo">
                <a href="#"><img height="30" src="../assets/images/light-logo.png" alt="Logo"></a>
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
    }
}
</script>

<style lang="scss">
header {
    background-color: #1F2154;
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
            border: 1px solid white;
            border-top-left-radius: 5px;
            border-bottom-left-radius: 5px;
            background: white;
            height: 48px;
            width: 50%;
            padding-left: 20px;
        }
        button {
            border: 1px solid white;
            background-color: white;
            color: #1fad96;
            border-top-right-radius: 5px;
            border-bottom-right-radius: 5px;
            height: 48px;
            width: 48px;
        }
    }
}   
</style>