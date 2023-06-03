<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      message: "",
    };
  },
  methods: {
    submitForm() {
      if (this.name && this.email && this.message) {
        // Menggunakan Formsprees untuk mengirim email
        window.formspree.submitForm("contactForm", {
          name: this.name,
          email: this.email,
          message: this.message,
        });

        // Reset form setelah pengiriman
        this.name = "";
        this.email = "";
        this.message = "";

        console.log("Form berhasil dikirim");
      } else {
        console.log("Form tidak lengkap");
      }
    },
  },
};
</script>
<template>
  <div class="flex justify-center py-[80px]">
    <div class="max-w-md w-full px-4 py-8 bg-black shadow-lg rounded-lg">
      <h1 class="text-3xl font-bold mb-4 text-white">Halaman Kontak</h1>
      <form @submit.prevent="submitForm">
        <!-- Isi form di sini -->
        <form>
          <div class="mb-4">
            <label for="name" class="block text-white text-sm font-bold mb-2">Nama</label>
            <input v-model="name" type="text" id="name" name="name" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" />
          </div>

          <div class="mb-4">
            <label for="email" class="block text-white text-sm font-bold mb-2">Email</label>
            <input v-model="email" type="email" id="email" name="_replyto" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" />
          </div>

          <div class="mb-4">
            <label for="message" class="block text-white text-sm font-bold mb-2">Pesan</label>
            <textarea v-model="message" id="message" name="message" rows="5" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"></textarea>
          </div>

          <div class="flex items-center justify-end">
            <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">Kirim</button>
          </div>
        </form>
      </form>
    </div>
  </div>
</template>
