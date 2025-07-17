<template>
  <NuxtLayout/>
</template>

<style>
html{
  font-family: "Montserrat";
  font-weight: 500;
  color: white;
}

@font-face {
  font-family: "Montserrat";
  font-style: normal;
  font-display: swap;
  src: url(/assets/fonts/Montserrat.ttf);
}

.page_padding{
  padding-left: 6rem;
  padding-right: 6rem;
}

@media screen and (max-width: 1260px) {
  .page_padding{
    padding-left: 2rem;
    padding-right: 2rem;
  }
}

@media screen and (max-width: 768px) {
  .page_padding{
    padding-left: 1rem;
    padding-right: 1rem;
  }
}
</style>
