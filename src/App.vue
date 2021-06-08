<template>
  <vue-form-wrapper
    :realtime="false"
    @form-item-change="formItemChange"
    @form-button-clicked="formButtonClicked"
    class="form"
  >
    <h5>Send me a message</h5>
    <p>please enter your details in the form bellow</p>
    <span>
      Name:
      <input ref="name" type="text" placeholder="Name" />
    </span>
    <span>
      Email:
      <input ref="email" type="email" placeholder="Email" />
    </span>
    <span>
      Number:
      <input ref="phone" type="tel" placeholder="Phone" />
    </span>

    <button ref="button">Send Message</button>
  </vue-form-wrapper>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({})
export default class App extends Vue {

  public formItemChange(formField: any): void {
    console.log(formField);
  }

  public formButtonClicked(form: any): void {
    console.log(form);
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@100;400;500;900&display=swap");
.form {
  font-family: "Roboto", sans-serif;
  display: flex;
  flex-direction: column;
  max-width: 300px;
  margin: 0 auto;
  align-content: space-around;
}
.form span {
  margin: 10px 0;
  display: flex;
  justify-content: space-between;
}
</style>
