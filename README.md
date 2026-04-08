# abi-techinnovation / ai-research-map

AI/ML 研究分野マップ 2025-2026 のインタラクティブナレッジグラフを GitHub Pages で公開する**暫定的な**リポジトリ。

## 公開 URL

# [https://abi-techinnovation.github.io/ai-research-map/](https://abi-techinnovation.github.io/ai-research-map/)

ブラウザでアクセスすればナレッジグラフが直接表示される。インストール・ログイン不要。

## このリポジトリの位置づけ

**研究テーマ把握を目的とした暫定運用** のリポジトリ。
将来的に **mkdocs** ベースの本格的な部署ナレッジサイトに移行する予定。それまでの間、AI 研究分野マップの可視化だけを最小構成で公開する。

- 機能拡張や汎用化はしない（カード型ハブ・サイドバー・複数ナレッジ管理などは行わない）
- 中身は AI 研究分野マップ KG ビューア 1 つのみ
- 移行先サイトが立ち上がったら、本リポジトリは archive 化 or 削除する

## 中身

| ファイル | 役割 |
|---|---|
| `index.html` | KG ビューア本体 (vis-network 9.1.13 を HTML 内インライン、依存なし) |
| `README.md` | このファイル |

## 公開しているナレッジグラフ

### AI/ML 研究分野マップ 2025-2026

- **テーマ数**: 236
- **エッジ数**: 564 (Theme 間 RELATED_TO)
- **カテゴリ数**: 8

| # | カテゴリ | テーマ数 |
|---|---|---:|
| 1 | 基盤技術 | 26 |
| 2 | 自然言語処理 | 24 |
| 3 | コンピュータビジョン | 28 |
| 4 | 生成 AI | 30 |
| 5 | AI エージェント | 29 |
| 6 | 応用分野 | 39 |
| 7 | インフラ / MLOps | 30 |
| 8 | 安全性 / 倫理 | 30 |

## ビューアの操作方法

| 操作 | 動作 |
|---|---|
| ドラッグ | 視点移動 |
| ホイール | ズームイン / アウト |
| ノードクリック | 右パネルに詳細 (説明・キーワード・関連テーマ) |
| 関連テーマクリック | そのノードへジャンプ |
| 上部検索ボックス | 名前 / サブカテゴリ / キーワードでハイライト |
| 左サイドのチェック | カテゴリ / 強度フィルタ |
| リセットボタン | 全表示に戻す |

## 更新方法

KG ビューアを更新したら、以下のコマンドで再デプロイする：

```bash
cd ~/git/abi-knowledge-base   # ローカルディレクトリ名は履歴上の名残
cp /path/to/new/kg-viewer.html index.html
git add index.html
git commit -m "Update KG viewer ($(date +%Y-%m-%d))"
git push
```

数十秒後に GitHub Pages 経由で自動反映される。

## 技術スタック

- **可視化**: vis-network 9.1.13 (HTML 内インライン、CDN ゼロ)
- **データ生成元**: Kuzu (LPG) + rdflib (RDF/Turtle 並列出力)
- **構築スキル**: `kg-builder` Claude Code skill
- **配信**: GitHub Pages (Public, 無料)

## 関連リソース

- **R&D ラボリポジトリ**: [rnd-lab-team-ocho-v202604](https://github.com/abi-techinnovation/rnd-lab-team-ocho-v202604)
- **個人ナレッジベース** (別物): `~/knowledge-base/` (SessionEnd フック自動蓄積)
- **個人 GitHub knowledge-base** (別物): `toshiaki0311/knowledge-base`

## 移行予定

| 項目 | 想定 |
|---|---|
| 移行先 | mkdocs (Material テーマ) を想定 |
| 移行時期 | 部署ナレッジサイト本格化のタイミング |
| 移行内容 | 本リポジトリの KG ビューアは新サイト内の 1 ページとして組み込む |
| 廃止後 | 本リポジトリは archive、URL は新サイトへリダイレクト |

## ライセンス・公開範囲

- リポジトリは Public (URL を知っていれば誰でも閲覧可能)
- 含まれるのは AI/ML の公知技術情報のみ
- 機密情報・顧客情報・社内固有情報は一切含めない
