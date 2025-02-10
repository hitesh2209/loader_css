<style>
    .all_loader {
        display: flex;
        gap: 100px;
        margin: 30px;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: baseline;
    }

 

    /*-----------------loader1-------------------*/
    .loader1 {
        width: 50px;
        aspect-ratio: 1;
        display: grid;
        border: 4px solid #0000;
        border-radius: 50%;
        border-color: #ccc #0000;
        animation: l16 1s infinite linear;
    }

    .loader1::before,
    .loader1::after {
        content: "";
        grid-area: 1/1;
        margin: 2px;
        border: inherit;
        border-radius: 50%;
    }

    .loader1::before {
        border-color: #f03355 #0000;
        animation: inherit;
        animation-duration: .5s;
        animation-direction: reverse;
    }

    .loader1::after {
        margin: 8px;
    }

    @keyframes l16 {
        100% {
            transform: rotate(1turn)
        }
    }

    /*-----------------loader2-------------------*/

    .loader2 {
        width: 50px;
        aspect-ratio: 1;
        border-radius: 50%;
        background: #000000;
        -webkit-mask: radial-gradient(circle closest-side at 50% 40%, #0000 94%, #000);
        transform-origin: 50% 40%;
        animation: l25 1s infinite linear;
    }

    @keyframes l25 {
        100% {
            transform: rotate(1turn)
        }
    }


    /*-----------------loader3-------------------*/


    .loader3 {
        width: 50px;
        aspect-ratio: 1;
        display: grid;
        border: 4px solid #0000;
        border-radius: 50%;
        border-right-color: #25b09b;
        animation: l15 1s infinite linear;
    }

    .loader3::before,
    .loader3::after {
        content: "";
        grid-area: 1/1;
        margin: 2px;
        border: inherit;
        border-radius: 50%;
        animation: l15 2s infinite;
    }

    .loader3::after {
        margin: 8px;
        animation-duration: 3s;
    }

    @keyframes l15 {
        100% {
            transform: rotate(1turn)
        }
    }

    /*-----------------loader4-------------------*/

    .loader4 {
        font-weight: bold;
        font-family: sans-serif;
        font-size: 30px;
        animation: l1 1s linear infinite alternate;
    }

    .loader4:before {
        content: "Loading..."
    }

    @keyframes l1 {
        to {
            opacity: 0
        }
    }


    /*-----------------loader5-------------------*/



    .loader5 {
        --d: 22px;
        width: 4px;
        height: 4px;
        border-radius: 50%;
        color: #25b09b;
        box-shadow:
            calc(1*var(--d)) calc(0*var(--d)) 0 0,
            calc(0.707*var(--d)) calc(0.707*var(--d)) 0 1px,
            calc(0*var(--d)) calc(1*var(--d)) 0 2px,
            calc(-0.707*var(--d)) calc(0.707*var(--d)) 0 3px,
            calc(-1*var(--d)) calc(0*var(--d)) 0 4px,
            calc(-0.707*var(--d)) calc(-0.707*var(--d))0 5px,
            calc(0*var(--d)) calc(-1*var(--d)) 0 6px;
        animation: l27 1s infinite steps(8);
    }

    @keyframes l27 {
        100% {
            transform: rotate(1turn)
        }
    }

    /*-----------------loader6-------------------*/




    .loader6 {
        width: 40px;
        aspect-ratio: 1;
        display: grid;
    }

    .loader6::before,
    .loader6::after {
        content: "";
        grid-area: 1/1;
        background: orange;
        clip-path: polygon(0 0, 101% 0, 0 100%);
        animation: l13 2s infinite;
    }

    .loader6::after {
        --s: -1, -1;
    }

    @keyframes l13 {

        0%,
        10% {
            transform: scale(var(--s, 1)) translate(0, 0) rotate(0deg)
        }

        33% {
            transform: scale(var(--s, 1)) translate(20px, -20px) rotate(0deg)
        }

        66% {
            transform: scale(var(--s, 1)) translate(20px, -20px) rotate(180deg)
        }

        90%,
        100% {
            transform: scale(var(--s, 1)) translate(0px, 0px) rotate(180deg)
        }
    }


    /*-----------------loader7-------------------*/

    .loader7 {
        width: 60px;
        aspect-ratio: 1.154;
        --c: #0000, #25b09b 2deg 59deg, #0000 61deg;
        --c1: conic-gradient(from 149deg at top, var(--c));
        --c2: conic-gradient(from -31deg at bottom, var(--c));
        background:
            var(--c1) top,
            var(--c1) bottom right,
            var(--c2) bottom,
            var(--c1) bottom left;
        background-size: 50% 50%;
        background-repeat: no-repeat;
        animation: l37 1s infinite;
    }

    @keyframes l37 {

        80%,
        100% {
            background-position: bottom right, bottom left, bottom, top
        }
    }

    /*-----------------loader8-------------------*/

    .loader8 {
        --c: no-repeat linear-gradient(orange 0 0);
        background:
            var(--c), var(--c), var(--c),
            var(--c), var(--c), var(--c),
            var(--c), var(--c), var(--c);
        background-size: 16px 16px;
        animation:
            l32-1 1s infinite,
            l32-2 1s infinite;
    }

    @keyframes l32-1 {

        0%,
        100% {
            width: 45px;
            height: 45px
        }

        35%,
        65% {
            width: 65px;
            height: 65px
        }
    }

    @keyframes l32-2 {

        0%,
        40% {
            background-position: 0 0, 0 50%, 0 100%, 50% 100%, 100% 100%, 100% 50%, 100% 0, 50% 0, 50% 50%
        }

        60%,
        100% {
            background-position: 0 50%, 0 100%, 50% 100%, 100% 100%, 100% 50%, 100% 0, 50% 0, 0 0, 50% 50%
        }
    }

    /*-----------------loader9-------------------*/


    .loader9 {
        display: inline-flex;
        width: 90px;
        aspect-ratio: 2;
        animation: l10-0 1s linear infinite;
    }

    .loader9:before,
    .loader9:after {
        content: "";
        flex: 1;
        background: #574951;
        clip-path: polygon(50% 0, 100% 50%, 50% 100%, 0 50%);
        animation: l10-1 1s linear infinite;
        transform-origin: right;
    }

    .loader9:after {
        scale: -1 1;
        translate: -100% 0;
        animation-direction: reverse;
    }

    @keyframes l10-0 {
        0% {
            translate: 0 -35.35%
        }

        to {
            translate: 0 35.35%
        }
    }

    @keyframes l10-1 {
        0% {
            rotate: -45deg
        }

        to {
            rotate: 45deg
        }
    }


    /*-----------------loader10-------------------*/

    .loader10 {
        --s: 20px;

        --_d: calc(0.353*var(--s));
        width: calc(var(--s) + var(--_d));
        aspect-ratio: 1;
        display: grid;
    }

    .loader10:before,
    .loader10:after {
        content: "";
        grid-area: 1/1;
        clip-path: polygon(var(--_d) 0, 100% 0, 100% calc(100% - var(--_d)), calc(100% - var(--_d)) 100%, 0 100%, 0 var(--_d));
        background:
            conic-gradient(from -90deg at calc(100% - var(--_d)) var(--_d),
                #fff 135deg, #666 0 270deg, #aaa 0);
        animation: l6 2s infinite;
    }

    .loader10:after {
        animation-delay: -1s;
    }

    @keyframes l6 {
        0% {
            transform: translate(0, 0)
        }

        25% {
            transform: translate(30px, 0)
        }

        50% {
            transform: translate(30px, 30px)
        }

        75% {
            transform: translate(0, 30px)
        }

        100% {
            transform: translate(0, 0)
        }
    }

    /*-----------------loader11-------------------*/

    .loader11 {
        width: 120px;
        height: 20px;
        border-radius: 20px;
        background:
            linear-gradient(orange 0 0) 0/0% no-repeat lightblue;
        animation: l2 2s infinite steps(10);
    }

    @keyframes l2 {
        100% {
            background-size: 110%
        }
    }



    /*-----------------loader12-------------------*/

    .loader12 {
        --r1: 154%;
        --r2: 68.5%;
        width: 60px;
        aspect-ratio: 1;
        border-radius: 50%;
        background:
            radial-gradient(var(--r1) var(--r2) at top, #0000 79.5%, #269af2 80%),
            radial-gradient(var(--r1) var(--r2) at bottom, #269af2 79.5%, #0000 80%),
            radial-gradient(var(--r1) var(--r2) at top, #0000 79.5%, #269af2 80%),
            #ccc;
        background-size: 50.5% 220%;
        background-position: -100% 0%, 0% 0%, 100% 0%;
        background-repeat: no-repeat;
        animation: l9 2s infinite linear;
    }

    @keyframes l9 {
        33% {
            background-position: 0% 33%, 100% 33%, 200% 33%
        }

        66% {
            background-position: -100% 66%, 0% 66%, 100% 66%
        }

        100% {
            background-position: 0% 100%, 100% 100%, 200% 100%
        }
    }

    /*-----------------loader13-------------------*/

    .loader13 {
        width: 120px;
        height: 22px;
        border-radius: 20px;
        color: #514b82;
        border: 2px solid;
        position: relative;
    }

    .loader13::before {
        content: "";
        position: absolute;
        margin: 2px;
        inset: 0 100% 0 0;
        border-radius: inherit;
        background: currentColor;
        animation: l6 2s infinite;
    }

    @keyframes l6 {
        100% {
            inset: 0
        }
    }

    /*-----------------loader14-------------------*/

    .loader14 {
        width: 60px;
        aspect-ratio: 1;
        border-radius: 50%;
        animation: l11 2s infinite;
    }

    @keyframes l11 {
        0% {
            background: conic-gradient(#f03355 0, #0000 0)
        }

        12.5% {
            background: conic-gradient(#f03355 45deg, #0000 46deg)
        }

        25% {
            background: conic-gradient(#f03355 90deg, #0000 91deg)
        }

        37.5% {
            background: conic-gradient(#f03355 135deg, #0000 136deg)
        }

        50% {
            background: conic-gradient(#f03355 180deg, #0000 181deg)
        }

        62.5% {
            background: conic-gradient(#f03355 225deg, #0000 226deg)
        }

        75% {
            background: conic-gradient(#f03355 270deg, #0000 271deg)
        }

        87.5% {
            background: conic-gradient(#f03355 315deg, #0000 316deg)
        }

        100% {
            background: conic-gradient(#f03355 360deg, #0000 360deg)
        }
    }



    /*-----------------loader15-------------------*/
    /* HTML: <div class="loader"></div> */
    .loader15 {
        width: 60px;
        aspect-ratio: 1;
        border: 15px solid #ddd;
        border-radius: 50%;
        position: relative;
        transform: rotate(45deg);
    }

    .loader15::before {
        content: "";
        position: absolute;
        inset: -15px;
        border-radius: 50%;
        border: 15px solid #514b82;
        animation: l18 2s infinite linear;
    }

    @keyframes l18 {
        0% {
            clip-path: polygon(50% 50%, 0 0, 0 0, 0 0, 0 0, 0 0)
        }

        25% {
            clip-path: polygon(50% 50%, 0 0, 100% 0, 100% 0, 100% 0, 100% 0)
        }

        50% {
            clip-path: polygon(50% 50%, 0 0, 100% 0, 100% 100%, 100% 100%, 100% 100%)
        }

        75% {
            clip-path: polygon(50% 50%, 0 0, 100% 0, 100% 100%, 0 100%, 0 100%)
        }

        100% {
            clip-path: polygon(50% 50%, 0 0, 100% 0, 100% 100%, 0 100%, 0 0)
        }
    }

    /*-----------------loader16-------------------*/
    
.loader16 {
  width: 20px;
  aspect-ratio: 1;
  border-radius: 50%;
  position: relative;
  transform-origin: 50% -200%;
  background: radial-gradient(at 30% 30%,#0000,#000a) red;
  animation: l8 1s cubic-bezier(.5,-200,.5,200) infinite;
}
.loader16:before {
  content: "";
  position: absolute;
  inset: -200% 8px 100%;
  background: #ddd; 
}
@keyframes l8 { 
    100% {transform:rotate(1deg)} 
}
    
    
    /*-----------------loader17-------------------*/
    
    
.loader17 {
  width: 120px;
  height: 22px;
  border-radius: 40px;
  color: #514b82;
  border: 2px solid;
  position: relative;
}
.loader17::before {
  content: "";
  position: absolute;
  margin: 2px;
  width: 25%;
  top: 0;
  bottom: 0;
  left: 0;
  border-radius: inherit;
  background: currentColor;
  animation: l3 1s infinite linear;
}
@keyframes l3 {
    50% {left:100%;transform: translateX(calc(-100% - 4px))}
}
    /*-----------------loader18-------------------*/
    
    
.loader18 {
  width: fit-content;
  font-size: 40px;
  font-family: system-ui,sans-serif;
  font-weight: bold;
  text-transform: uppercase;
  color: #0000;
  -webkit-text-stroke: 1px #000;
  background: conic-gradient(#000 0 0) 0/0% 100% no-repeat text;
  animation: l1 1s linear infinite;
}
.loader18:before {
  content: "Loading";
}
@keyframes l1 {
  to{background-size: 120% 100%}
}
    /*-----------------loader19-------------------*/
    
.loader19 {
  width: 60px;
  aspect-ratio: .5;
  display: grid;
}
.loader19:before {
  content: "";
  width: 30%;
  aspect-ratio: 1;
  border-radius: 50%;
  margin: auto auto 0;
  background: #CF4647;
  animation: l9-0 .5s cubic-bezier(0,800,1,800) infinite;
}
.loader19:after {
  content: "";
  width: 100%;
  aspect-ratio: 1/cos(30deg);
  margin: 0 auto auto;
  clip-path: polygon(50% -50%,100% 50%,50% 150%,0 50%);
  background: #524656;
  animation: l9-1 .5s linear infinite;
}
@keyframes l9-0 {
  0%,2%  {translate: 0   0%}
  98%,to {translate: 0 -.2%}
}
@keyframes l9-1 {
  0%,5%  {rotate:  0deg}
  95%,to {rotate:-60deg}
}
    

    /*-----------------loader20-------------------*/
    
 
.loader20 {
  height: 60px;
  aspect-ratio: 2;
  border-bottom: 3px solid #0000;
  background: 
    linear-gradient(90deg,#524656 50%,#0000 0)
    -25% 100%/50% 3px repeat-x border-box;
  position: relative;
  animation: l3-0 .75s linear infinite;
}
.loader20:before {
  content: "";
  position: absolute;
  inset: auto 42.5% 0;
  aspect-ratio: 1;
  border-radius: 50%;
  background: #CF4647;
  animation: l3-1 .75s cubic-bezier(0,900,1,900) infinite;
}
@keyframes l3-0 {
  to {background-position: -125% 100%}
}
@keyframes l3-1 {
  0%,2% {bottom: 0%}
  98%,to {bottom:.1%}
}

</style>



<div class="all_loader">


    <div class="loader1"></div>
    <div class="loader2"></div>
    <div class="loader3"></div>
    <div class="loader4"></div>
    <div class="loader5"></div>
    <div class="loader6"></div>
    <div class="loader7"></div>
    <div class="loader8"></div>
    <div class="loader9"></div>
    <div class="loader10"></div>
    <div class="loader11"></div>
    <div class="loader12"></div>
    <div class="loader13"></div>
    <div class="loader14"></div>
    <div class="loader15"></div>
    <div class="loader16"></div>
    <div class="loader17"></div>
    <div class="loader18"></div>
    <div class="loader19"></div>
    <div class="loader20"></div>

</div>
