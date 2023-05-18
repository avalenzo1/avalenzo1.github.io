<template>
  <NuxtLayout>
    <Header />
    <NuxtPage />
    <Footer />
  </NuxtLayout>
</template>

<script>
  // import VWave from 'v-wave'

  // Vue.use(VWave);
  // function cursorPointer() {
  //   let cursor = document.createElement("div");
  //       cursor.classList.add("an-cursor");

  //   document.addEventListener("mousemove", function(e) {
  //     cursor.style.left = e.clientX - 12.5 + "px";
  //     cursor.style.top = e.clientY - 12.5 + "px";
  //   });

  //   document.addEventListener("touchmove", function(e) {
  //     cursor.style.left = e.touches[0].clientX - 12.5 + "px";
  //     cursor.style.top = e.touches[0].clientY - 12.5 + "px";
  //   });

  //   document.addEventListener("click", function(e) {
  //     cursor.classList.add("an-cursor--click");
  //   });

  //   document.addEventListener("animationend", (e) => {
  //     cursor.classList.remove("an-cursor--click");
  //   });

  //   document.body.appendChild(cursor);
  // }

  // cursorPointer();
</script>