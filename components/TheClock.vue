<template>
<div class="clock">
    <div class="hour" v-bind:style="{transform: 'rotate(' + hourDeg + ')'}" style="transform: rotate(30deg);"></div>
    <div class="min" v-bind:style="{transform: 'rotate(' + minsDeg + ')'}" style="transform: rotate(252deg);"></div>
    <div class="sec" v-bind:style="{transform: 'rotate(' + secsDeg + ')'}" style="transform: rotate(36deg);"></div>
</div>
</template>

<script>
export default {
    data() {
        return {
            appTitle: 'Vue Clock',
            hour: '--',
            hourDeg: '0deg',
            mins: '--',
            minsDeg: '0deg',
            secs: '--',
            secsDeg: '0deg'
        }

    },
    created() {
        this.updateClock();
    },
    methods: {
        updateClock() {
            var ctx = this;
            setInterval(function () {
                var date = new Date(),
                    hour = date.getHours() + 1,
                    min = date.getMinutes(),
                    sec = date.getSeconds();

                // Set Display
                ctx.hour = (hour < 10) ? '0' + hour : hour;
                ctx.mins = (min < 10) ? '0' + min : min;
                ctx.secs = (sec < 10) ? '0' + sec : sec;

                // Set Analog
                var analogHour = (hour > 12) ? hour - 12 : hour,
                    analogMins = min,
                    analogSecs = sec;

                ctx.hourDeg = (analogHour * 30) + 'deg';
                ctx.minsDeg = (analogMins / 60 * 360) + 'deg';
                ctx.secsDeg = (analogSecs / 60 * 360) + 'deg';
            }, 1000);
        }
    }
}
</script>

<style lang="scss" scoped>
.clock {
    position: relative;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    border: solid 3px $color-primary;
    opacity: 0.2;
    transition: ease 250ms;

    &:hover {
        opacity: 1;
    }

    &::before {
        z-index: 3;
        content: '';
        position: absolute;
        top: 50%;
        left: 50%;
        width: 4px;
        height: 4px;
        transform: translate(-50%, -50%);
        background: $color-primary;
    }

    .hour,
    .min,
    .sec {
        z-index: 2;
        position: absolute;
        bottom: 50%;
        left: 50%;
        height: 40%;
        width: 4px;
        margin-left: -2px;
        background: $color-primary;
        transform-origin: bottom center;
        border-radius: 1px 1px 0 0;
    }

    .hour {
        height: 30%;
    }

    .sec {
        z-index: 1;
        height: 46%;
        left: 51%;
        width: 2px;
        background: $color-primary;
    }
}
</style>
