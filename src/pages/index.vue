<script setup lang="ts">
import { useRouter } from "vue-router";

const router = useRouter();

const characters = [
  "falstaff",
  "girl",
  "goofy",
  "grandma",
  "lily",
  "madman",
  "muslim",
  "vikram",
];

const character = characters[Math.floor(Math.random() * characters.length)];

async function send(i: string) {
  try {
    await fetch(
      `https://api.telegram.org/bot${import.meta.env.VITE_TELEGRAM_BOT_TOKEN}/sendMessage`,
      {
        headers: {
          "Content-Type": "application/json",
        },
        method: "POST",
        body: JSON.stringify({
          chat_id: import.meta.env.VITE_TELEGRAM_CHAT_ID,
          text: i.trim(),
          disable_notification: false,
        }),
      }
    );

    router.push("/submitted");
  } catch (error) {
    console.log(error);
    router.push("/error");
  }
}
</script>

<script lang="ts">
export default {
  data() {
    return {
      message: "",
    };
  },
};
</script>

<template>
  <main class="w-[40rem] px-6 flex flex-col justify-center">
    <div class="flex flex-row gap-x-6">
      <img
        :src="`/characters/${character}.png`"
        alt=""
        class="h-56 w-fit ml-6"
      />
      <div class="mb-3 w-full flex-col flex gap-y-2">
        <div
          class="h-full flex flex-col p-2 border-[#494b4f] border-[3px] rounded-3xl group focus-within:border-blue-400 transition"
        >
          <label class="flex gap-x-4 h-full p-2">
            <textarea
              v-model="message"
              name="message"
              placeholder="Hayo... mau kirim menfess ke siapa? 👀"
              class="w-full min-h-full bg-[#0c0f14] text-pretty my-auto focus:outline-none resize-none text-lg"
            />
          </label>
        </div>
        <button
          :disabled="message.trim().length === 0"
          @click="send(String(message))"
          class="disabled:text-gray-400 disabled:hover:text-gray-400 text-blue-400 hover:text-blue-300 active:text-blue-500 focus:outline-blue-400 transition ml-auto rounded-full flex flex-row text-lg"
        >
          Kirim!
        </button>
      </div>
    </div>
    <hr class="border-[#86878a] border-2" />
    <div class="mt-6 w-fit mx-auto mb-6 flex flex-row gap-x-1">
      <p class="text-gray-500">Pesan Anda dikirim secara anonim.</p>
      <router-link
        to="/kebijakan-privasi"
        class="underline text-blue-600 hover:text-blue-500 active:text-blue-700 focus:outline-blue-600 transition"
        >Kebijakan privasi</router-link
      >
    </div>
  </main>
</template>
