# tailwind css post css 構築

### # postCSS、tailwindCSS 　インストール

- npm install -D tailwindcss postcss autoprefixer

### # Tailwind CSS の設定ファイルを生成

- npx tailwindcss init

### # CSS ファイルをビルド

- npx postcss ./src/style.css -o ./dist/style.css

# 勉強ノート

### # 優先順位（競合）

### エントリーポイント VS インラインクラス(in vue)

- エントリーポイント css ファイルにカスタマイズクラスを追加することを vue ファイルで使うことができる。
- div の class 属性にカスタマイズクラスをつけたら css が適用されるけど、それとは別に text-blue-500 などをつけても反映されない。
- エントリーポイント CSS === vue ファイルのタグ class 属性

### エントリーポイント VS style scoped タグ(in vue)

- style タグの優先順位が高いため、エントリーポイントで書かれているスタイルが上書きされる。
- もちろん被らないスタイルに関してはエントリーポイントのスタイルが適用される。
- エントリーポイント < style scoped

### エントリーポイント VS インラインスタイル(in vue)

- div タグのなかの style 属性にスタイル指定すると style 属性のスタイルが適用される。
- エントリーポイント < インラインスタイル

### インラインスタイル VS style scoped

- インラインスタイルが優先順位が高いため、style タグが適用される。
- inline style > style scoped
