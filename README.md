# AFTER NINE — GitHub Pages

ジャグラーの実戦判断トレーニング教材。無料・ログイン不要。v1.1公開準備版。

## 公開

専用のPublicリポジトリ `kazuhiro4869/after-nine-trainer` を使用する。
`index.html`・`.nojekyll`・このREADMEをリポジトリのルートに配置する。
ビルド・外部ライブラリ・データベースは不要。

GitHubの Settings > Pages で以下を指定する。

- Source: Deploy from a branch
- Branch: main
- Folder: /(root)

公開予定URL: https://kazuhiro4869.github.io/after-nine-trainer/
このURLはPagesの公開完了と実アクセスを確認するまで利用可能とは限らない。

## 2026-10-16 修正と検証

- 問題画面の関数に混入していたHTMLを修正し、JavaScriptの構文エラーを解消。
- 未定義だった見出しを「着席判断トレーニング」「経過判断シミュレーション」と問題番号に変更。答えを誘導するサブタイトルは回答後のみ表示。
- `.nojekyll`を追加し、静的ファイルとして配信する構成にした。
- Node.jsの隔離実行環境で全30ケース・50判断画面の遷移、回答と解説、事前分布の切替、記録の保存・再読み込み、共有データ生成、コピーによる共有の代替動作を検証。
- 全ケースのモデル計算132組を直接の尤度計算と照合。各設定の確率合計・加重平均の範囲を確認。
- 3機種のBB・REG確率、出玉率を北電子公式製品ページと照合済み。
- 公開サイト、iPhoneサイズの実描画、LINEアプリへの引き渡しは別途ブラウザ確認が必要。

## 教材としての前提

架空データを用いた非公式の教材。設定分布はBB・REG公表確率と選択した事前分布によるモデル上の推定値。
実際の設定、勝率、実収益を保証しない。参考判断の一致率を実戦の勝率・設定的中率として扱わない。
学習記録は利用中のブラウザのlocalStorageへ保存する。端末間の同期は行わない。

出典:

- https://www.kitadenshi.co.jp/slot/myjuggler5/
- https://www.kitadenshi.co.jp/slot/neoimjugglerex/
- https://www.kitadenshi.co.jp/slot/gogojuggler3/
