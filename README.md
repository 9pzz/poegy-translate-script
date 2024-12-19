### 패스오브엑자일 거래소 한글화스크립트

사용방법
1. 아래 스크립트를 복사
```
(async function translateTradeWebsite() {
  const url =
    "https://raw.githubusercontent.com/9pzz/poegy-translate-script/master/script.js";

  try {
    const response = await fetch(url);

    if (!response.ok) {
      throw new Error(`Error: ${response.statusText}`);
    }
    const data = await response.text();
    eval(data);

    console.log("성공! 새로고침을 해주세요");
  } catch (error) {
    console.error("에러 ", error);
  }
})();
```
2. 패스오브엑자일 영문거래소 접속
- https://poe.game.daum.net/trade2/search/poe2/Standard 우측 상단 영국국기클릭
- https://www.pathofexile.com/trade2
3. F12 -> 콘솔 또는 Console 항목 클릭
4. 복사한 스크립트를 붙혀넣기 (Ctrl+V)하고 `성공!` 메시지가 뜨면 페이지 새로고침

오류
- Warning: Don' t paste code into ~~ 뜨는 경우
  - `allow pasting` 또는 `붙여넣기 허용`을 입력하고 다시 스크립트 붙혀넣기

다시 영문으로 돌리는방법
- 개발자도구(F12) -> 애플리케이션 -> 좌측 [저장용량][로컬스토리지][poe거래소링크] 클릭 -> 중앙 상단 🚫 클릭, 새로고침
