# LeeDDHH resume

[![textlint](https://img.shields.io/github/workflow/status/LeeDDHH/resume/lint%20text?label=textlint&logo=github&color=yellow)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22lint+text%22)
[![build pdf](https://img.shields.io/github/workflow/status/LeeDDHH/resume/build-pdf?label=build%20pdf&logo=github)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22build+pdf%22)
[![create issue](https://img.shields.io/github/workflow/status/LeeDDHH/resume/create%20issue?label=create%20issue&logo=github&color=orange)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22create+issue%22)
[![release date](https://img.shields.io/github/release-date/LeeDDHH/resume?color=blue&logo=github)](https://github.com/LeeDDHH/resume/releases)

[ 日本語 | [English](https://github.com/LeeDDHH/resume/blob/main/README.en.md) ]

## Data

- [PDF](https://github.com/LeeDDHH/resume/releases)
- [File](https://github.com/LeeDDHH/resume/blob/main/resume/README.md)

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
