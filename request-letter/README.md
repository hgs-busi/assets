# 인포그래픽 의뢰 우편함 (병합·닫기 금지)

이 브랜치와 이 브랜치의 Pull Request는 `hgs-busi/stock_blog` 파이프라인의 **의뢰서 우편함**이다.

- GPT(Codex) 파이프라인이 `request-letter/YYYY/MM/DD/<kind>.request.md`를 이 브랜치에 push한다
- 그 push 이벤트가 Claude 감시 세션을 깨우고, Claude가 인포그래픽을 만들어 `main`의 `stock_blog/YYYY/MM/DD/<kind>.png`·`<kind>.meta.json`으로 올린다
- 게시 이력이 기록되면 GPT가 이 브랜치의 의뢰서와 `main`의 메타를 지운다

**이 PR을 병합하거나 닫지 말 것.** 닫히는 순간 감시가 끝난다. 프로토콜 정본은 `stock_blog/docs/request-letter.md`.
