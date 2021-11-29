<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-6">
                    <div class="address">
                        <h4>Address</h4>
                        <div class="info">
                            <p>382 NE 191st St # 87394 Miami, FL 33179-3899</p>
                            <p>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</p>
                            <p><a href="#" class="email">support@maxcoach.com</a></p>
                        </div>
                    </div>
                    <div class="socials">
                        <div class="social"><i class="fab fa-facebook-square"></i></div>
                        <div class="social"><i class="fab fa-twitter"></i></div>
                        <div class="social"><i class="fab fa-instagram"></i></div>
                        <div class="social"><i class="fab fa-linkedin"></i></div>
                    </div>
                </div>
                <div class="col-6 d-flex">
                    <div class="explore">
                        <h4>Explore</h4>
                        <ul class="link_explore">
                            <li v-for="linkExplore in explore" :key="linkExplore.linkEx"><a href="#">{{ linkExplore }}</a></li>
                        </ul>
                    </div>
                    <div class="information">
                        <h4>Information</h4>
                        <ul class="link_information">
                            <li v-for="linkInformation in information" :key="linkInformation.linkInfo"><a href="#">{{ linkInformation }}</a></li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="copyright">
                
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'SiteFooter',
    props: {
        explore: Array,
        information: Array
    }
}
</script>

<style lang="scss">
footer {
    background-color: #f8f8f8;
    padding: 80px 0;
    h4 {
        font-size: 18px;
        font-weight: bold;
        margin-bottom: 20px;
    }
    .address {
        .info {
            font-size: 14px;
            margin-bottom: 25px;
            .email {
                text-decoration: none;
                color: #212529;
                &:hover {
                    color: #1fad96;
                }
            }
        }
    }
    .socials {
        display: flex;
        .social {
            margin-right: 30px;
        }
        i {
            color: #b1b1b1;
            font-size: 24px;
            cursor: pointer;
            &:hover {
                color: #1fad96;
            }
        }
    }
    .explore,
    .information {
        ul {
            list-style: none;
            padding: 0;
            font-size: 14px;
            line-height: 35px;
            a {
                text-decoration: none;
                color: #212529;
                &:hover {
                    color: #1fad96;
                }
            }
        }
    }
    .link_explore {
        display: flex;
        flex-wrap: wrap;
        flex-direction: column;
        height: 50%;
        li {
            margin-right: 80px;
        }
    }
    .information {
        margin-left: 140px;
    }
}
</style>