<template>
    <div class="login-wrapper col-sm-8">
        <Header/>
        <h4>Login</h4>
        <div class="shadow-none p-3 mb-5 bg-light rounded">
            <form action="">
                <div>
                    <input v-model="message1" placeholder="modifiez-mo1">
                    <p>message1 : {{ message1 }}</p>
                </div>
                <div>
                    <input v-model="message2" placeholder="modifiez-moi2">
                    <p>message2: {{ message2 }}</p>
                </div>
                <div>
                    <input type="range"
                    min="0"
                    max="100"
                    step="10"
                    v-model="value">
                </div>
                <div> <vue-range-slider ref="slider" v-model="value"></vue-range-slider></div>
            </form>
             <!-- <button v-on:click="more = !more">test</button>
                <div v-if="more">
                    plus d'information
                </div> -->
               
        </div>
    </div>
</template>
<script>
import './statics/Login.css'
import Header from '../components/Header'
import 'vue-range-component/dist/vue-range-slider.css'
import VueRangeSlider from 'vue-range-component'
export default {
    name:'Login',
    components:{Header,VueRangeSlider},
    data(){
        return{
            message1:'',
            message2:'',
            more:false,
            value:[20,60]
        }
    }
}
</script>