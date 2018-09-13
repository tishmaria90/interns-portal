<template>
    <div class="enter-form">
        <form>
            <el-input type="email" placeholder="Email" v-model="input"></el-input>
            <el-input type="password" placeholder="Password" v-model="input">
                <el-button slot="append" icon="el-icon-view"></el-button>
            </el-input>   
            <el-button>Войти</el-button>
        </form>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
