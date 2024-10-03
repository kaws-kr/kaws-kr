<div style="display: flex; justify-content: center; gap: 10px;">
  <img id="stats" src="https://github-readme-stats.vercel.app/api?username=kaws-kr&show_icons=true&theme=dark&count_private=true&locale=kr" width="400" height="200"/>
  <img id="langs" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kaws-kr&langs_count=20&layout=compact" width="400" height="200"/>
</div>

<script>
  const statsImg = document.getElementById('stats');
  const langsImg = document.getElementById('langs');

  // 다크모드 감지
  const darkModeQuery = window.matchMedia('(prefers-color-scheme: dark)');
  function updateTheme(e) {
    if (e.matches) {
      statsImg.src = "https://github-readme-stats.vercel.app/api?username=kaws-kr&show_icons=true&theme=dark&count_private=true&locale=kr";
      langsImg.src = "https://github-readme-stats.vercel.app/api/top-langs/?username=kaws-kr&langs_count=20&layout=compact&theme=dark";
    } else {
      statsImg.src = "https://github-readme-stats.vercel.app/api?username=kaws-kr&show_icons=true&theme=default&count_private=true&locale=kr";
      langsImg.src = "https://github-readme-stats.vercel.app/api/top-langs/?username=kaws-kr&langs_count=20&layout=compact&theme=default";
    }
  }

  // 페이지 로드 시 초기 테마 설정
  updateTheme(darkModeQuery);

  // 테마 변경 시 업데이트
  darkModeQuery.addListener(updateTheme);
</script>
