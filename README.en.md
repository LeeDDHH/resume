# LeeDDHH resume

[![textlint](https://img.shields.io/github/workflow/status/LeeDDHH/resume/lint%20text?label=textlint&logo=github&color=yellow)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22lint+text%22)
[![build pdf](https://img.shields.io/github/workflow/status/LeeDDHH/resume/build-pdf?label=build%20pdf&logo=github)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22build+pdf%22)
[![create issue](https://img.shields.io/github/workflow/status/LeeDDHH/resume/create%20issue?label=create%20issue&logo=github&color=orange)](https://github.com/LeeDDHH/resume/actions?query=workflow%3A%22create+issue%22)
[![release date](https://img.shields.io/github/release-date/LeeDDHH/resume?color=blue&logo=github)](https://github.com/LeeDDHH/resume/releases)

[ [日本語](https://github.com/LeeDDHH/resume/blob/main/README.md) | English ]

## Data

- [PDF](https://github.com/LeeDDHH/resume/releases)
- [File](https://github.com/LeeDDHH/resume/blob/master/docs/README.md)

## Features

### 💅 Lint text

- Automatic proofreading with [textlint](https://github.com/textlint/textlint).

```
yarn fix
```

- It is also automatically executed when pre-commit by [lefthook](https://github.com/evilmartians/lefthook).
- proofreading rules are set with `.textlintrc`.

### 📝 Convert MD to PDF

- You can generate PDF with [md-to-pdf](https://github.com/simonhaenisch/md-to-pdf).

```
yarn build
```

- The output PDF can be styled as you like with CSS.
  - Edit the `pdf-configs/style.css`.
- The output directory is `resume` by default.

### 🛠 Create release

- When you push with a `v**` tag, GitHub Actions will run the build, generate the PDF, create a Release, and register the PDF to Assets.

```
git commit -m "add job"
git tag v1.0
git push origin --tags
```

### 📆 Remind update

- Automatically generate issues every three months with GitHub Actions Schedules triggers to prompt you to update your resume.
- To change the duration or stop the job, edit `.github/workflows/create-issue.yml`.
- To change the issue contents, edit `.github/issue_template.md`.
