---
description: フロントエンドエンジニア御用達
---

# Gulp

## 概要

### 公式サイト

{% embed data="{\"url\":\"https://gulpjs.com/\",\"type\":\"link\",\"title\":\"gulp.js\",\"icon\":{\"type\":\"icon\",\"url\":\"https://gulpjs.com/img/favicon.png\",\"aspectRatio\":0}}" %}

Gulpは昨今のフロントエンド開発では必須とえる以下の作業を行うためのツールです。

* ローカルサーバー
* scssのコンパイル
* JSや画像の結合、圧縮
* ファイルの変更検知
* 各種ファイルのLint（コードチェック）

## クイックスタート

gulpコマンドのインストール

```bash
$ npm i -g gulp-cli
```

プロジェクトディレクトリに移動（あるいはプロジェクトディレクトリをVSCで開いた状態でVSCのターミナルで操作してください）

```bash
cd <プロジェクトディレクトリ>
```

package.json の作成

```bash
$ npm init -y
```

Gulpおよび関連ツールのインストール

```bash
$ npm i gulp gulp-sass browser-sync gulp-imagemin gulp-plumber
```

gulpfile.jsの作成

{% code-tabs %}
{% code-tabs-item title="gulpfile.js" %}
```javascript
const gulp = require('gulp');
const sass = require('gulp-sass');
const watch = require('gulp-watch');
const watch = require('gulp-watch');
const plumber = require('gulp-plumber');

const path = {
  src: './src',
  dist: './docs'
}

gulp.task('sass', () => {
  return gulp.src('./src/**/*.scss')
    .pipe(plumber())
    .pipe(sass().on('error', sass.logError))
    .pipe(gulp.dest('./dist'));
});

gulp.task('default', ['serve'], () => {
  browserSync({
    server: {
      baseDir: path.dist,
    }
  });
});

gulp.task('watch', () => {
  watch('./src/**/*.scss', () => {
    gulp.start('sass')
  });

  watch(path.dist, () => {
    browserSync.reload();
  });
});
```
{% endcode-tabs-item %}
{% endcode-tabs %}

gulpの起動

```bash
$ gulp
```

## Tips

ready...



