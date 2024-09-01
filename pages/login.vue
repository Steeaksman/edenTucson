<script setup>
const client = useSupabaseAuthClient();
const router = useRouter();

const email = ref('')
const password = ref(null);
const errorMsg = ref(null);
// const successMsg = ref(null);

async function signIn() {
     
        try {
        const { error} = await client.auth.signInWithPassword({
            email: email.value,
            password: password.value,
        });
        if (error) throw error;
        router.push("/profile");
     } catch (error) {
     errorMsg.value = error.message;
    }
}

</script>

<template>
    <form class="row flex-center flex" @submit.prevent="handleLogin">
      <div class="col-6 form-widget">
        <h1 class="header">Supabase + Nuxt 3</h1>
        <p class="description">Sign in  email below</p>
        <div>
          <input class="inputField" type="password" placeholder="password" v-model="email" />
        </div>
        
        <div>
          <input class="inputField" type="email" placeholder="Your email" v-model="email" />
        </div>
        <div>
          <input
            type="submit"
            class="button block"
            :value="loading ? 'Loading' : 'Send magic link'"
            :disabled="loading"
          />
        </div>
      </div>
    </form>
  </template>