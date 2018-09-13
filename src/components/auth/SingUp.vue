<template>
    <div class="enter-form">
        <form @submit.prevent="submit">
            <el-input type="text" placeholder="Имя" v-model="input"></el-input>
            <el-input type="text" placeholder="Фамилия" v-model="input"></el-input>
            <el-input type="text" min="3" placeholder="Логин" v-model="input"></el-input>
            <el-input type="email" placeholder="Email" v-model="input"></el-input>
            <el-input :type="type" min="6" placeholder="Password" v-model="input">
                <el-button @click.prevent="$emit('togglePassword')" slot="append" icon="el-icon-view"></el-button>
            </el-input>   
            <el-button native-type="submit">Зарегистрироваться</el-button>
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
            input: ''
        }
    },
    methods: {
        submit(){
            console.log("+++++");            
        }
    }
}
</script>

<style>

</style>
