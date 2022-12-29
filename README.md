# {name} resume

[![textlint](https://img.shields.io/github/workflow/status/{name}/resume/lint%20text?label=textlint&logo=github&color=yellow)](https://github.com/{name}/resume/actions?query=workflow%3A%22lint+text%22)
[![build pdf](https://img.shields.io/github/workflow/status/{name}/resume/build-pdf?label=build%20pdf&logo=github)](https://github.com/{name}/resume/actions?query=workflow%3A%22build+pdf%22)
[![create issue](https://img.shields.io/github/workflow/status/{name}/resume/create%20issue?label=create%20issue&logo=github&color=orange)](https://github.com/{name}/resume/actions?query=workflow%3A%22create+issue%22)
[![release date](https://img.shields.io/github/release-date/{name}/resume?color=blue&logo=github)](https://github.com/{name}/resume/releases)

[ 日本語 | [English](https://github.com/{name}/resume/blob/main/README.en.md) ]

## Sample

- 自分の GitHub の ID が `LeeDDHH` の場合
  - <https://github.com/LeeDDHH/resume>

## Data

- [PDF](https://github.com/{name}/resume/releases)
- [File](https://github.com/{name}/resume/blob/master/docs/README.md)

## Make Icon

- 技術系のアイコンを作る場合
  - [Simple Icons](https://simpleicons.org/)
  - [Shields.io: Quality metadata badges for open source projects](https://shields.io/)
  - [shields.io で技術系のアイコンをたくさん作ってみる | 404 motivation not found](https://tech-blog.s-yoshiki.com/entry/150/?referer=https://t.co/)

## Features

### 💅 Lint text

[textlint](https://github.com/textlint/textlint)での自動校正が可能です。

```
yarn fix
```

- [lefthook](https://github.com/evilmartians/lefthook)によって commit 前にも自動で実行されます。
- 校正のルールは `.textlintrc` に記載しています。

### 📝 Convert MD to PDF

[md-to-pdf](https://github.com/simonhaenisch/md-to-pdf)での PDF 生成が可能です。

```
yarn build
```

- 出力される PDF は CSS で任意のスタイルを設定可能です。
  - スタイルは `pdf-configs/style.css` を編集してください。
- 出力先はデフォルトで `resume` ディレクトリになります。

### 🛠 Create release

- `v**` tag をつけて push すると GitHub Actions でビルドが走り、PDF の生成、Release の作成、Assets へ PDF の登録が実行されます。

```
git commit -m "add job"
git tag v1.0
git push origin --tags
```

### 📆 Remind update

- GitHub Actions の schedule trigger で 3 ヶ月に 1 回、職務経歴書の内容更新を促す issue が自動生成されます。
- 期間の変更、Job の停止は `.github/workflows/create-issue.yml` を編集してください。
- 生成される issue の中身は `.github/issue_template.md` を編集してください。
