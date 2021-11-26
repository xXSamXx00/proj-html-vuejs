<template>
    <main>
        <div class="hero_image">
            <div class="text-center">
                <h1>Learn At Your Own Pace!</h1>
                <p>Get teamed up with people of the same will.</p>
                <button class="button mb-5">Get started for free</button>
            </div>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" preserveAspectRatio="none">
                <path class="elementor-shape-fill" opacity="0.33" d="M473,67.3c-203.9,88.3-263.1-34-320.3,0C66,119.1,0,59.7,0,59.7V0h1000v59.7 c0,0-62.1,26.1-94.9,29.3c-32.8,3.3-62.8-12.3-75.8-22.1C806,49.6,745.3,8.7,694.9,4.7S492.4,59,473,67.3z"></path>
                <path class="elementor-shape-fill" opacity="0.66" d="M734,67.3c-45.5,0-77.2-23.2-129.1-39.1c-28.6-8.7-150.3-10.1-254,39.1 s-91.7-34.4-149.2,0C115.7,118.3,0,39.8,0,39.8V0h1000v36.5c0,0-28.2-18.5-92.1-18.5C810.2,18.1,775.7,67.3,734,67.3z"></path>
                <path class="elementor-shape-fill" d="M766.1,28.9c-200-57.5-266,65.5-395.1,19.5C242,1.8,242,5.4,184.8,20.6C128,35.8,132.3,44.9,89.9,52.5C28.6,63.7,0,0,0,0 h1000c0,0-9.9,40.9-83.6,48.1S829.6,47,766.1,28.9z"></path>
            </svg>
            <div class="thumb_image mt-4">
                <img class="position-absolute left_image" src="../assets/images/home-6-hero-left-person.png" alt="Donna al computer">
                <div class="main_image">
                    <img class="position-relative" src="../assets/images/home-6-hero-poster-final.jpg" alt="Hero Image">
                    <div class="youtube_play">
                        <img src="../assets/images/icon-youtube-play.png" alt="Youtube play">
                    </div>
                </div>
                <img class="position-absolute right_image" src="../assets/images/home-6-hero-right-person.png" alt="Donna al computer">
            </div>
        </div>
        <div class="next"></div>
    </main>
</template>

<script>
export default {
    name: 'SiteMain',

}
</script>

<style lang="scss">
.hero_image {
    padding-top: 80px;
    background-color: #1F2154;
    color: white;
    height: 650px;
    position: relative;
    h1 {
        font-weight: 600;
    }
    .button {
        background-color: #1fad96;
        color: white;
        border: 1px solid #1fad96;
        border-radius: 5px;
        padding: 12px 30px;
        font-size: 12px;
        font-weight: 600;
        transition: 0.5s;
        &:hover {
            color: #1fad96;
            background-color: white;
        }
    }
    svg {
        position: absolute;
        bottom: 0;
        transform: rotate(180deg);
        display: block;
        width: calc(100% + 1.3px);
        height: 654px;
        z-index: -1;
        path {
            fill: rgba(255, 255, 255, 0.04);
        }
    }
    .thumb_image {
        position: relative;
        .main_image {
            position: absolute;
            display: inline-block;
            border: 15px solid white;
            border-radius: 15px;
            left: 50%;
            transform: translate(-50%);
            .youtube_play {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
            }
        }
        .left_image {
            left: 218px;
            top: -42px;
        }
        .right_image {
            left: 1335px;
            top: 285px;
        }
    }
}
.next {
    height: 600px;
    background-color: #f6f3f6;
}
</style>