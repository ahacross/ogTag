<template>
  <main>
    <h1>Og Tag Test</h1>
    <a href="https://www.opengraph.xyz/" target="_blank">
      태그 만드는 사이트(opengraph.xyz)
    </a>
    <br />
    <br />
    <a
      href="https://developers.kakao.com/tool/debugger/sharing"
      target="_blank"
    >
      카카오 테스트 페이지
    </a>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
