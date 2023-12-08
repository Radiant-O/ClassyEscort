<script lang="ts" setup>
import { ref, reactive } from "vue";
import { useRouter } from "vue-router";

const router = useRouter()
interface FormState {
  username: string;
  password: string;
  remember: boolean;
}
const active = ref(false);

const formState = reactive<FormState>({
  username: "",
  password: "",
  remember: true,
});
const onFinish = async (values: any) => {
  active.value = true;
  const credentials = {

    user_name: formState.username,

    password: formState.password,
  };
  setTimeout( () => {
    active.value = false
  }, 10000);
  await router.push({ name: "home" });
};

</script>

<template>
  <div class="land">
    <section class="img lg:block hidden">
      <div class="reg_img">
        <img src="../assets/images/u.jpeg" alt="" />
      </div>
    </section>
    <section class="reg">
      <div class="reg_form">
        <div class="reg_top">
          <p class="font-normal pt-5 text-xl">Welcome to ClassyEscorts...</p>
          <p class="reg_top_text">Sign In</p>
          
        </div>
        <a-form
          :model="formState"
          name="basic"
          @finish="onFinish"
          
        >
          <a-form-item
            label="Username"
            class="form_input"
            name="username"
            :rules="[
              { required: true, message: 'Please input your username!' },
            ]"
          >
            <a-input v-model:value="formState.username" />
          </a-form-item>

          <a-form-item
            label="Password"
            class="form_input pass_form"
            name="password"
            :rules="[
              { required: true, message: 'Please input your password!' },
            ]"
          >
            <a-input-password v-model:value="formState.password" />
          </a-form-item>
          <div class="loading">
          <div class="loader" v-if="active">
            <a-spin />
          </div>
        </div>
          <a-form-item :wrapper-col="{ offset: 12, span: 16 }">
            <a-button class="reg_btn" html-type="submit">Submit</a-button>
          </a-form-item>
        </a-form>
      </div>
    </section>
  </div>
</template>

<style scoped>
.real {
  @apply w-full h-full;
}
.land {
  @apply lg:flex block w-[90%] lg:h-[70%] pb-[10rem] mx-[5%] mt-[5%] justify-between items-center border rounded-tr-[6rem] rounded-bl-[6rem] bg-pink-400;
}
.img {
  @apply w-[50%];
}
.reg_img img {
  @apply w-[30rem] mx-auto my-[4rem];
}
.reg {
  @apply lg:w-[50%] w-full;
}
.reg_form {
  @apply lg:w-[30rem] w-[85%] mx-auto lg:mx-0  lg:h-[20rem] h-full;
}
.reg_form a-form {
  @apply m-auto;
}
.reg_top_text {
  @apply lg:text-center font-semibold text-3xl lg:p-0 pl-5 pt-5;
}
.reg_btn {
  @apply -ml-8 lg:-ml-0 bg-white text-black font-semibold cursor-pointer;
}
.reg_btn:hover {
  @apply bg-white text-black font-semibold cursor-pointer;
}
.form_input{
  @apply py-2 text-2xl font-normal 
}
.pass_form{
  @apply -mt-5 lg:-mt-0
}
</style>
