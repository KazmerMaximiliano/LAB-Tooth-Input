<template>
    <div>
        <div class="tooth-input">
            <div 
                class="top-tooth" 
                :class="tooth[0].active ? `${tooth[0].color}` : ''" 
                @click="setTooth(0)"
            ></div>
            <div 
                class="right-tooth" 
                :class="tooth[1].active ? `${tooth[1].color}` : ''" 
                @click="setTooth(1)"
            ></div>
            <div 
                class="bottom-tooth" 
                :class="tooth[2].active ? `${tooth[2].color}` : ''" 
                @click="setTooth(2)"
            ></div>
            <div 
                class="left-tooth" 
                :class="tooth[3].active ? `${tooth[3].color}` : ''" 
                @click="setTooth(3)"
            ></div>
            <div 
                class="center-tooth"
                :class="tooth[4].active ? `${tooth[4].color}` : ''" 
                @click="setTooth(4)"
            ></div>
        </div>
    </div>
</template>

<script>
import './toothInput.scss';

export default {
    data: () => ({
        tooth: [
            {
                active: false,
                color: 'red',
                state: 'Carie'
            },
            {
                active: false,
                color: 'red',
                state: 'Carie'
            },
            {
                active: false,
                color: 'red',
                state: 'Carie'
            },
            {
                active: false,
                color: 'red',
                state: 'Carie'
            },
            {
                active: false,
                color: 'red',
                state: 'Carie'
            }
        ]
    }),

    methods: {
        setTooth(i) {
            this.tooth[i].active = !this.tooth[i].active;
            // console.log(this.tooth);
        }
    }
}
</script>

<style>

</style>