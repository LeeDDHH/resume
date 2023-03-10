# LeeDDHH resume

[![textlint](https://img.shields.io/github/workflow/status/LeeDDHH/resume/lint%20text?label=textlint&logo=github&color=yellow)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22lint+text%22)
[![build pdf](https://img.shields.io/github/workflow/status/LeeDDHH/resume/build-pdf?label=build%20pdf&logo=github)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22build+pdf%22)
[![create issue](https://img.shields.io/github/workflow/status/LeeDDHH/resume/create%20issue?label=create%20issue&logo=github&color=orange)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22create+issue%22)
[![release date](https://img.shields.io/github/release-date/LeeDDHH/resume?color=blue&logo=github)](https://github.com/LeeDDHH/resume/releases)

[ æ¥æ¬èª | [English](https://github.com/LeeDDHH/resume/blob/main/README.en.md) ]

## Data

- [PDF](https://github.com/LeeDDHH/resume/releases)
- [File](https://github.com/LeeDDHH/resume/blob/main/resume/README.md)

## Features

### ð Lint text

[textlint](https://github.com/textlint/textlint)ã§ã®èªåæ ¡æ­£ãå¯è½ã§ãã

```
yarn fix
```

- [lefthook](https://github.com/evilmartians/lefthook)ã«ãã£ã¦ commit åã«ãèªåã§å®è¡ããã¾ãã
- æ ¡æ­£ã®ã«ã¼ã«ã¯ `.textlintrc` ã«è¨è¼ãã¦ãã¾ãã

### ð Convert MD to PDF

[md-to-pdf](https://github.com/simonhaenisch/md-to-pdf)ã§ã® PDF çæãå¯è½ã§ãã

```
yarn build
```

- åºåããã PDF ã¯ CSS ã§ä»»æã®ã¹ã¿ã¤ã«ãè¨­å®å¯è½ã§ãã
  - ã¹ã¿ã¤ã«ã¯ `pdf-configs/style.css` ãç·¨éãã¦ãã ããã
- åºååã¯ããã©ã«ãã§ `resume` ãã£ã¬ã¯ããªã«ãªãã¾ãã

### ð  Create release

- `v**` tag ãã¤ãã¦ push ããã¨ GitHub Actions ã§ãã«ããèµ°ããPDF ã®çæãRelease ã®ä½æãAssets ã¸ PDF ã®ç»é²ãå®è¡ããã¾ãã

```
git commit -m "add job"
git tag v1.0
git push origin --tags
```

### ð Remind update

- GitHub Actions ã® schedule trigger ã§ 3 ã¶æã« 1 åãè·åçµæ­´æ¸ã®åå®¹æ´æ°ãä¿ã issue ãèªåçæããã¾ãã
- æéã®å¤æ´ãJob ã®åæ­¢ã¯ `.github/workflows/create-issue.yml` ãç·¨éãã¦ãã ããã
- çæããã issue ã®ä¸­èº«ã¯ `.github/issue_template.md` ãç·¨éãã¦ãã ããã
