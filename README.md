# abi-techinnovation / knowledge-base

技術革新部 R&D ラボのナレッジグラフを GitHub Pages で公開するリポジトリ。

## 公開 URL

[https://abi-techinnovation.github.io/knowledge-base/](https://abi-techinnovation.github.io/knowledge-base/)

ブラウザでクリックすればナレッジグラフがインタラクティブに表示される。

## 現在公開しているナレッジグラフ

### AI/ML 研究分野マップ 2025-2026

- **テーマ数**: 236 (8 カテゴリ)
- **エッジ数**: 564 (Theme 間 RELATED_TO)
- **データソース**: AI 研究分野マップ Markdown ドキュメント
- **更新日**: 2026-04-08

8 カテゴリ:
1. 基盤技術 (26 テーマ)
2. 自然言語処理 (24 テーマ)
3. コンピュータビジョン (28 テーマ)
4. 生成 AI (30 テーマ)
5. AI エージェント (29 テーマ)
6. 応用分野 (39 テーマ)
7. インフラ / MLOps (30 テーマ)
8. 安全性 / 倫理 (30 テーマ)

## ビューアの使い方

| 操作 | 動作 |
|---|---|
| ドラッグ | 視点移動 |
| ホイール | ズームイン / アウト |
| ノードクリック | 右パネルに詳細 (説明・キーワード・関連テーマ) |
| 関連テーマクリック | そのノードへジャンプ |
| 上部検索ボックス | 名前 / サブカテゴリ / キーワードでハイライト |
| 左サイドのチェック | カテゴリ / 強度フィルタ |
| リセットボタン | 全表示に戻す |

## 技術スタック

- **可視化**: vis-network 9.1.13 (HTML 内インライン)
- **データ生成**: Kuzu (Labeled Property Graph) + rdflib (RDF/Turtle 並列出力)
- **配信**: GitHub Pages (静的ホスティング)
- **デザイン**: ダークテーマ統一

## 関連リソース

- **元データ**: 別途管理されている AI 研究分野マップ 2025-2026 Markdown
- **構築スキル**: `kg-builder` (Claude Code skill)
- **R&D ラボリポジトリ**: [rnd-lab-team-ocho-v202604](https://github.com/abi-techinnovation/rnd-lab-team-ocho-v202604)

## 更新方法

KG ビューアを更新したら、以下のコマンドで再デプロイする：

```bash
cd ~/git/abi-knowledge-base
cp /path/to/new/kg-viewer.html index.html
git add index.html
git commit -m "Update KG viewer ($(date +%Y-%m-%d))"
git push
```

GitHub Pages が自動で再ビルドして 1 分以内に反映される。

## ライセンス

社内利用を想定。外部公開時は別途検討。
