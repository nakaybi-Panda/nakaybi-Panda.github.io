# 喋る煽りパンダ — GitHub Pages公開用

## 公開に含まれる機能

- スマートフォン向けチャット画面とパンダのタップ反応
- 録音済みの反応音声
- 設定からON/OFFできる端末の日本語システム音声読み上げ
- 入力欄内のマイクボタンによる音声入力（ブラウザー対応時）
- 「パンダにインムキング流して」「INMU KING流して」の入力・音声認識による曲再生
- PWAのホーム画面追加、Service Workerによる初回アクセス後のオフライン利用

## 公開手順

1. このZIPを展開し、中身（`index.html`、`audio/`、`icons/`、`.github/`など）をGitHubリポジトリのルートへ置きます。`public/`フォルダーを作って中へ入れるのではなく、`index.html`がリポジトリ直下に来るようにしてください。
2. `main`ブランチへコミット・pushします。
3. GitHubリポジトリの **Settings → Pages → Build and deployment → Source** で **GitHub Actions** を選択します。
4. **Actions** タブの `Deploy PWA to GitHub Pages` が成功すると、同画面またはSettings → Pagesに公開URLが表示されます。

`.github/workflows/pages.yml`は`main`へのpushごとに静的サイトを自動公開します。データベースやサーバーは不要です。

## 注意

- 初回表示後、Service Workerがファイルをキャッシュするまで一度オンライン接続が必要です。
- マイク入力はブラウザーの音声認識対応とマイク許可が必要です。音声認識は一部ブラウザーで利用できない場合があります。
- システム音声の種類は端末・ブラウザーにより異なります。
- `audio/inmu-king.mp3`も公開アセットに含まれます。公開前にこの音源を公開する権利があることをご確認ください。
