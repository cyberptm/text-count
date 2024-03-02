<template>
  <main>
    <div class="text-center flex flex-col justify-center h-screen">
      <div class="mb-16">
        <h1 class="text-3xl mb-4 text-zinc-800">文字数カウント</h1>
        <textarea cols="50" rows="5" class="border rounded-xl border-zinc-200 bg-zinc-50 px-3 py-2.5 text-zinc-800" v-model="text"></textarea>
        <div class="text-zinc-700 text-xs mt-2">※ 改行も１文字としてカウントされます。</div>
        <div class="text-zinc-700 text-xs mt-1">※ 一部のマルチバイト文字は１文字で２文字以上分カウントされる場合があります。</div>

        <div class="mt-4">
          <div class="text-zinc-700 text-sm">現在の文字数</div>
          <div class="text-zinc-800 text-3xl mt-1 font-medium">{{text.length}}文字</div>
        </div>
      </div>
    </div>
  </main>

  <div class="absolute bottom-4 flex justify-center w-screen">
    <a href="https://cyberptm.pages.dev/">
      <img src="/cyberptm_logo.svg" alt="Cyberphantom" class="h-14 inline">
    </a>
  </div>
</template>

<script>
export default{
  data(){
    return{
      text: ""
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP&display=swap')

@tailwind base;
@tailwind components;
@tailwind utilities;

*{
  font-family: "Noto Sans JP", sans-serif;
}
</style>