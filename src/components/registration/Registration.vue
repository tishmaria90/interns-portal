<template>
  <div class="registration-page">

    <div class="registration-main-block">
      <logo className="logo_registration-page"/>
      <div class="registration-form">
        <div class="registration-form__header">
          <button @click="toggleComponent">{{ toggle ? 'Войти' : 'Зарегистрироваться' }}</button>
        </div>
        <div class="registration-form__body">
          <component @togglePassword="togglePassword" :type="type" :is="toggle ? 'sing-in' : 'sing-up'"></component>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
  import SingIn from '@/components/auth/SingIn'
  import SingUp from '@/components/auth/SingUp'
  import Logo from '@/components/logo/Logo'
  import '@/assets/sass/components/logo.sass'

  export default {
    components: {
      SingIn,
      SingUp,
      Logo
    },
    data() {
      return {
        toggle: true,
        type: 'password'
      }
    },
    methods: {
      toggleComponent() {
        this.toggle = !this.toggle
      },
      togglePassword() {        
        this.type = this.type == 'password' ? 'text' : 'password';      
      }
    }
  }
</script>
<style lang="sass">
  
</style>
