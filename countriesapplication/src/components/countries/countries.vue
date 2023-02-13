<template>
    {{ data }}
</template>

<script>
import request from './request';

export default {
    data(){
        return{
            data: [],
        }
    },
    methods: {
        async getAllCountries(){
            const response = await fetch(request.getAllCountries);
            this.data = await response.json();
        }
    },
    created(){
        this.getAllCountries();
    }
}
</script>
