<template>
    <div class="enter-form">
        <form @submit.prevent="submit">
            <el-input type="email" placeholder="Email" v-model="input"></el-input>
            <el-input :type="type" placeholder="Password" v-model="input">
                <el-button @click.prevent="$emit('togglePassword')" slot="append" icon="el-icon-view"></el-button>
            </el-input>   
            <el-button native-type="submit">Войти</el-button>
        </form>
    </div>
</template>

<script>
export default {
    props: {
        type: {
            type: String,
            required: true
        }
    },
    data() {
        return {
            input: '',
        }
    },
    methods: {
        submit(){
            console.log('++++');            
        }
    }
}
</script>

<style>

</style>
