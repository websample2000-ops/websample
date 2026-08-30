# 活動者・配信者向け公式Webサイト テンプレート

GitHub PagesとGoogle Apps Script（GAS）を組み合わせ、**「維持費0円」**かつ**「専門知識不要で更新できる専用管理画面」**を実現したWebサイト制作テンプレートです。

🔗 **Demo Site:** [https://websample2000-ops.github.io/websample/](https://websample2000-ops.github.io/websample/)

---

## 📌 開発の背景・解決した課題
個人VTuberや配信者が自身のWebサイトを持つ際、主に以下の課題が存在します。
1. **コストの壁**: レンタルサーバー代やドメイン代などの固定維持費が発生する
2. **運用の壁**: WordPress等の導入・保守やコード編集のハードルが高い

本プロジェクトでは、静的ホスティング（GitHub Pages）とヘッドレスCMS構成（GAS × Googleスプレッドシート）を組み合わせることで、**ランニングコスト完全0円**かつ**スマホやPCからブログ感覚で更新可能なシステム**を構築しました。

---

## 🛠 主な機能
- **レスポンシブデザイン**: PC・スマートフォン・タブレットの各端末に最適化
- **専用管理画面連携**:
  - GoogleスプレッドシートをマスターDBとして活用
  - GASで構築したAPI経由で「お知らせ」「動画一覧」「ショップ情報」「ガイドライン」を即時同期
- **導線最適化**: 各種SNS・配信プラットフォーム・二次創作ガイドラインへの直感的なナビゲーション

---

## 💻 使用技術（Tech Stack）
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla JS / ES6+)
- **Backend / API**: Google Apps Script (REST API設計)
- **Database / CMS**: Google Sheets
- **Hosting**: GitHub Pages

---

## ⚙️ システム構成・アーキテクチャ
1. 管理画面（またはスプレッドシート）からデータを登録・編集
2. GAS（Web Apps）がJSON形式でエンドポイントへデータを配信
3. フロントエンド（JavaScript / Fetch API）が非同期でデータを取得し、DOMへ動的レンダリング
