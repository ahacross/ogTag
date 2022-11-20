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
      카카오 OG 캐시 삭제 사이트
    </a>
    <br />
    <br />
    <button @click="shareKakao">카카오 공유하기</button>
  </main>
</template>
<script>
export default {
  methods: {
    shareKakao() {
      window.Kakao.Share.sendDefault({
        objectType: 'feed',
        content: {
          title: '딸기 치즈 케익',
          description: '#케익 #딸기 #삼평동 #카페 #분위기 #소개팅',
          imageUrl:
            'http://k.kakaocdn.net/dn/Q2iNx/btqgeRgV54P/VLdBs9cvyn8BJXB3o7N8UK/kakaolink40_original.png',
          link: {
            // [내 애플리케이션] > [플랫폼] 에서 등록한 사이트 도메인과 일치해야 함
            mobileWebUrl: 'https://developers.kakao.com',
            webUrl: 'https://developers.kakao.com',
          },
        },
        social: {
          likeCount: 286,
          commentCount: 45,
          sharedCount: 845,
        },
        buttons: [
          {
            title: '네이버로 보기',
            link: {
              mobileWebUrl: 'https://naver.com',
              webUrl: 'https://naver.com',
            },
          },
          {
            title: '앱으로 보기',
            link: {
              mobileWebUrl: 'https://developers.kakao.com',
              webUrl: 'https://developers.kakao.com',
            },
          },
        ],
      });
    },
  },
};
</script>

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
