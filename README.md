# 20-zodiac-fortune-wheel — 十二星座おみくじルーレット

## 概要
星座を選ぶとCanvasルーレットがアニメーション回転し、「宇宙的スケール」の大袈裟な運勢を表示するコメディアプリ。結果は履歴としてlocalStorageに保存。

## 機能
- 十二星座セレクター（アイコン・日付範囲付き）
- Canvasで12セクターのルーレットをイージングアニメーション回転
- 選択した星座に止まる（意図的に当選演出）
- 6段階の運勢ランク × 12種の宇宙的テキストをランダム組み合わせ
- 結果をlocalStorageに最大30件記録・履歴表示

## 技術仕様
- 静的SPA / Tailwind CDN
- Canvas 2D API（Arc/Sector/Text描画、RequestAnimationFrameイージング）
- localStorage キー: `zodiac_history`
- XSS対策: escapeHtml() 使用（innerHTML への挿入を全てエスケープ）
- a11y: aria-label / tabindex 対応
