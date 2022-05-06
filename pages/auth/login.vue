<template>
  <div>
    <!-- Head -->
    <headers/>
    <div>
      <!-- Form <headers />-->
    </div>

    Form
    <div>
       <b-form @submit="onSubmit" @reset="onReset" v-if="show">
        <b-form-group
          id="input-group-1"
          label="Адрес электронной почты"
          label-for="input-1"
        >
          <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            placeholder="Enter email"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Пароль" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.name"
            placeholder="Enter passwor"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-4" v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="form.checked"
            id="checkboxes-4"
            :aria-describedby="ariaDescribedby"
          >
            <b-form-checkbox value="true"
              >Запомнить меня на этом компьютере</b-form-checkbox
            >
          </b-form-checkbox-group>
        </b-form-group>
      </b-form>
      <b-card class="mt-3" header="Form Data Result">
        <pre class="m-0">{{ form }}</pre>
      </b-card> 
   </div>

    <!-- inputs -->
    <div>
      <b-form-group id="input">
      <form action="post">
        <div class="inp">
          <p>Адрес электронной почты</p>
          <forninput />
        </div>
        <div class="inp">
          <p>Адрес электронной почты</p>
          <forninput />
        </div>
      </form>
      </b-form-group>
    </div>
  </div>
</template>

<script>
import forninput from "~/components/forninput.vue";
import Headers from '~/components/headers.vue';
//import headers from "../components/headers.vue";
export default {
  components: { forninput, Headers },
  name: "login",
  data() {
    return {
      form: {
        email: "",
        name: "",
        checked: false,
      },
      show: true,
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(event) {
      event.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.food = null;
      this.form.checked = false;
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    },
  },
};
</script>

<style scoped>

</style>

