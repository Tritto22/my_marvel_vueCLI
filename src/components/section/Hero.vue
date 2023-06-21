<template>
    <div class="slider position-relative">
        <div class="header-hero d-flex justify-content-center align-items-center">
            <a href="#" class="text-uppercase text-decoration-none">stream ant-man and the wasp: quantumania on</a>
            <img src="../../assets/img/slider/logo_disney.png" alt="Disney logo">
        </div>
        <div 
        v-for="(hero,i) in slider" :key="i" 
        class="hero" :class="[((i == position) ? 'active' : 'disable'),(hero.name)]" 
        @mouseover="stopAutoplay()" @mouseleave="autoplay()"
        >
            <div class="container-info">
                <img 
                :src="hero.logo" 
                :alt="(i != 1) ? hero.name : ''" 
                :class="(i == 2 || i == 3) ? 'w_2' : 'w_1'"
                >
                <h1 class="text-uppercase">{{ hero.titol }}</h1>
                <p>{{ hero.description }}</p>
                <button class="fw-bold text-uppercase border-0" :class="(i == 4) ? 'disable' : 'active'">learn more</button>
            </div>
        </div>
        <div class="container-argument d-flex w-100 position-absolute z-1 bottom-0 start-50 translate-middle-x">
            <ul>
                <li 
                v-for="(element,i) in slider" :key="i" 
                class="fw-bold" :class="(i == position) ? 'underline' : ''"
                @click="select(i)"
                >
                    <div :class="(i == position) ? 'progress-bar' : ''"></div>
                    <a href="#" class="text-decoration-none d-flex">
                        {{ element.btn }}
                    </a>
                </li>
            </ul>
            <div class="social d-flex justify-content-center align-items-center">
                <font-awesome-icon :icon="['fab', 'facebook']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'twitter']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'instagram']" class="icon"/>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Hero',
    data(){
        return{
            slider: [
                {
                    name: 'spider',
                    btn: 'Marvel\'s Spider-Man 2 Pre-Orders',
                    logo: require('../../assets/img/slider/logo_1.png'),
                    titol: 'all about pre-orders',
                    description: 'We\'ve got all the details on pre- ordering Marvel\'s Spider - Man 2, plus an exclusive interview with Bryan Intihar, Creative Director at Insomniac Games!'
                },
                {
                    name: 'lee',
                    btn: 'Stan Lee Documentary Now Streaming',
                    logo: null,
                    titol: 'now streaming',
                    description: 'The original documentary \'Stan Lee\' is now streaming only on Disney+; we spoke to director and producer David Gelb about his work behind-the-scenes.'
                },
                {
                    name: 'new',
                    btn: 'This Week\'s New Comics',
                    logo: require('../../assets/img/slider/logo_3.png'),
                    titol: 'this week\'s new comics',
                    description: 'See a universe made anew, enter the Age of Monsters, witness the start to Contest of Chaos, and more in this week\'s comics!'
                },
                {
                    name: 'captain',
                    btn: 'A New Era Of Captain Marvel',
                    logo: require('../../assets/img/slider/logo_3.png'),
                    titol: 'a new era of captain marvel',
                    description: 'Check out the brand new costume for Carol Danvers\' new run by Alyssa Wong and Jan Bazaldua this October!'
                },
                {
                    name: 'avengers',
                    btn: 'Beyond Earth\'s Mightiest',
                    logo: require('../../assets/img/slider/logo_5.png'),
                    titol: 'celebrating 60 years of the avengers',
                    description: 'Milestone Celebration Includes All-New Avengers Products, Launch of Marvel Fit, and Sports Collaborations'
                }
            ],
            position: 0,
            autoplayID: null
        }
    },
    methods:{
        left: function () {
            if (this.position == 0) {
                this.position = this.slider.length - 1;
            } else {
                this.position--;
            }
        },
        right: function () {
            if (this.position == this.slider.length - 1) {
                this.position = 0;
            } else {
                this.position++;
            }
        },
        select: function (index) {
            this.position = index;
        },
        autoplay: function () {
            this.autoplayID = setInterval(this.right, 3000)
        },
        stopAutoplay: function () {
            clearInterval(this.autoplayID)
        }
    },
    mounted() {
        this.autoplay()
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import 'bootstrap';
.progress-bar {
  width: 0;
  height: 7px;
  background-color: #e62429;
  animation: progressAnimation 3s infinite;
}
@keyframes progressAnimation {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}
.active{
    display: block;
}
.disable{
    display: none;
}
.spider{
    background-image: url('../../assets/img/slider/hero_1.png');
}
.lee{
    background-image: url('../../assets/img/slider/hero_2.png');
}
.new{
    background-image: url('../../assets/img/slider/hero_3.png');
}
.captain{
    background-image: url('../../assets/img/slider/hero_4.png');
}
.avengers{
    background-image: url('../../assets/img/slider/hero_5.png');
}
.w_1{
    width: 300px;
}
.w_2{
    width: 150px;
}
.slider{
    height: 450px;
    .header-hero{
        background-color: #151515;
        a{
            color: white;
            font-size: 14px;
        }
        img{
            width: 70px;
        }
    }
    .hero{
        width: 100%;
        height: 440px;
        clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
        background-position: center;
        .container-info{
            padding: 20px 0 60px 150px;
            color: white;
            max-width: 830px;
            button{
                background-color: #e62429;
                color: white;
                font-size: 14px;
                padding: 15px 35px;
                clip-path: polygon(10% 0, 100% 0, 100% 70%, 90% 100%, 0 100%, 0 30%);
                &:hover{
                    background-color: #9f0013;
                }
            }
        }
    }
    .container-argument{
        max-width: 1240px;
        ul{
            width: 80%;
            display: flex;
            background-color: white;
            margin: 0;
            padding: 0;
            li{
                font-size: 14px;
                width: 20%;
                
                cursor: pointer;
                a{
                    color: black;
                    font-size: 14px;
                    padding: 12px 25px;
                }
            }
        }
        .social{
            width: 20%;
            .icon{
                margin-left: 25px;
                font-size: 20px;
                color: #767676;
                cursor: pointer;
                &:hover{
                    color: black;
                }
            }
        }
    }
}
</style>