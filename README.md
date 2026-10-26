# ClinicBasics 静的サイト（仮公開用）

**作成:** 2026-10-26（Asia/Tokyo）  
**公開ルート:** この `site/` ディレクトリ一式  
**アフィリエイトリンク:** **未掲載**（提携承認後に公式素材のみ追加）

## 含まれるページ

| パス | 内容 |
|------|------|
| `index.html` | ホーム・記事一覧・医療注意 |
| `about.html` | 運営方針 |
| `disclosure.html` | アフィリエイト開示 |
| `privacy.html` | 簡易プライバシー |
| `articles/01-first-visit-checklist.html` | 初診前チェック |
| `articles/02-how-to-read-costs.html` | 費用の見方 |
| `articles/03-online-vs-inperson.html` | オンラインと対面 |
| `articles/04-cancel-continue.html` | 解約・休薬・継続 |
| `articles/05-reading-official-sites.html` | 公式サイトの読み方 |
| `style.css` | 共通スタイル |

## 静的ホストへのデプロイ（例: Render Static Site）

1. このリポジトリ（または `clinicbasics/site` をルートにしたリポジトリ）を Git に載せる。
2. Render で **Static Site** を新規作成。
3. **Publish directory** を `clinicbasics/site`（またはこのフォルダをルートにした場合は `.`）に設定。
4. ビルドコマンドは不要（空で可）。静的 HTML のみ。
5. デプロイ後、Render が付与する `*.onrender.com` で仮公開を確認。

他の静的ホスト（Cloudflare Pages、Netlify、GitHub Pages、XServer の公開ディレクトリ等）でも、**この `site/` 配下をドキュメントルートに置く**だけで同じです。

## DNS（clinicbasics.jp）

- ドメイン `clinicbasics.jp` は **XServer Domain** で取得済み。
- ネームサーバー／DNS レコードはいま XServer Domain 側。
- 静的ホスト（Render 等）に本番接続する場合は、後から次のいずれかが必要です。
  - **CNAME:** `www` → ホスト指定のターゲット
  - **A / ALIAS / ANAME:**  apex（`clinicbasics.jp`）→ ホストの IP または指定レコード
- 仮公開段階では `*.onrender.com` 等のホストURLだけで十分な場合が多いです。DNS 切替は公開方針が固まってからで問題ありません。

## コンプライアンスメモ

- 記事冒頭に SITE.md 定型の開示文あり。各記事で「現時点リンクなし」も明記。
- 効果断定・ランキング・ビフォーアフター・他ブランド言及なし。
- 公開前チェックは `jp-clinic-compliance-checklist.md` を全 Yes で確認すること。
- 解析タグ・アフィリンク追加時は `privacy.html` / `disclosure.html` を更新すること。

## やらないこと（このディレクトリの範囲）

- デプロイ実行・DNS 変更・ブラウザ確認は別タスク。
- A8 等のアフィリエイトリンク挿入は提携承認後。
