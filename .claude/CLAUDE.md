# CLAUDE.md

## docs/voice/

### 前提
- `docs/voice` 配下（`index.html`, `data.js` など）はユーザー入力を受け付けない。データの供給源はスタッフが管理する静的な `data.js` のみ。

### レビュー時の注意
- `innerHTML` への値埋め込みに対する XSS 対策（エスケープ・`textContent` 化など）は指摘不要
- 将来的にフォームやコメント投稿などユーザー入力経路が追加された場合はこの前提を見直すこと
