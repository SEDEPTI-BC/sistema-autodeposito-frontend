<template>
  <div class="signup card p-4">
    <div class="brand text-center">
      <h1>
        <img
          src="~/static/img/logo.png"
          class="
            img-fluid
            ${3|rounded-top,rounded-right,rounded-bottom,rounded-left,rounded-circle,|}
          "
          alt="Autodeposite"
          title="Autodeposite"
          width="69"
          height="46"
        />
      </h1>
    </div>
    <form @submit.prevent="onSubmit">
      <small class="form-text text-muted text-center"
        >Campos obrigatórios são marcados com *</small
      >
      <div class="form-group">
        <label for="inputSignupName">Informe seu nome completo *</label>
        <input
          type="text"
          class="form-control mx-auto"
          name="inputSignupName"
          id="inputSignupName"
          v-model="$v.signupForm.name.$model"
          required
        />
      </div>
      <div class="form-group">
        <label for="inputSignupEmail">Informe seu email *</label>
        <input
          type="email"
          class="form-control mx-auto"
          name="inputSignupEmail"
          id="inputSignupEmail"
          v-model="$v.signupForm.email.$model"
          required
        />
      </div>
      <div class="form-group">
        <label for="inputSignupPassword">Crie sua senha *</label>
        <input
          type="password"
          class="form-control mx-auto"
          name="inputSignupPassword"
          id="inputSignupPassword"
          v-model="$v.signupForm.password.$model"
          required
        />
      </div>
      <div class="form-group">
        <label for="inputSignupPasswordConfirm">Confirme sua senha *</label>
        <input
          type="password"
          class="form-control mx-auto"
          name="inputSignupPasswordConfirm"
          id="inputSignupPasswordConfirm"
          v-model="$v.signupForm.passwordConfirm.$model"
          required
        />
        <div class="error" v-if="!$v.signupForm.passwordConfirm.sameAsPassword">
          As senhas devem ser iguais.
        </div>
      </div>

      <div class="form-group text-center">
        <!--TODO: deixar bonito os erros do form -->
        <button type="submit" class="btn btn-primary border-primary">
          Cadastrar
        </button>
      </div>
    </form>
  </div>
</template>

<style scoped>
.error {
  color: crimson;
  font-size: 0.8rem;
}
</style>>

</style>

<script>
import { required, minLength, sameAs, email } from 'vuelidate/lib/validators';
import '@nuxtjs/axios';

export default {
  name: 'Signup',
  data() {
    return {
      signupForm: {
        name: '',
        email: '',
        password: '',
        passwordConfirm: '',
      },
    };
  },
  validations: {
    signupForm: {
      name: {
        required,
        minLength: minLength(5),
      },
      email: {
        required,
        email,
      },
      password: {
        required,
        minLength: minLength(8),
      },
      passwordConfirm: {
        required,
        sameAsPassword: sameAs('password'),
      },
    },
  },
  methods: {
    async onSubmit() {
      if (this.$v.$invalid) {
        console.log('Form invalid');
      } else {
        this.$axios
          .post('/api/users', {
            username: this.signupForm.name,
            email: this.signupForm.email,
            password: this.signupForm.password,
            role: 'admin',
          })
          .then(() => console.log('USER CREATED'));
      }
    },
  },
};
</script>

