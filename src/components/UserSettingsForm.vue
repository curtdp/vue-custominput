<template>
  <form class="card" @submit.prevent="submit">
    <h1 class="text-2xl font-bold mb-6">Ваши настройки</h1>
    <label class="block mb-6">
      <span class="form-label mb-2">email адрес</span>
      <input :value="email" @input="email = $event.target.value.toUpperCase()" class="form-input" placeholder="you@example.com">
    </label>
    <div class="mb-8">
      <span class="form-label mb-2">Почтовая рассылка</span>
      <div class="flex justify-between items-center">
        <p class="mr-4">Подписаться на новости и обновления.</p>
          <toggle-input :value="receiveNewsletter"></toggle-input>
      </div>
    </div>
    <div class="text-right">
      <button type="submit" class="btn btn-blue">Сохранить настройки</button>
    </div>
  </form>
</template>

<script>
import ToggleInput from './ToggleInput.vue'

export default {
  components: {
    ToggleInput
  },
  data() {
    return {
      email: "igor@example.com",
      receiveNewsletter: false
    }
  },
  methods: {
    submit() {
      console.log("Отправка настроек...", {
        email: this.email,
        receiveNewsletter: this.receiveNewsletter
      })
    },
    toggleNewsletter() {
      this.receiveNewsletter = !this.receiveNewsletter
    }
  }
}
</script>
