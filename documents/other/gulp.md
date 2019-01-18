# Gulp

## 概要

### 公式サイト

{% embed url="https://gulpjs.com/" %}

Gulpは昨今のフロントエンド開発では必須とえる以下の作業を行うためのツールです。

* ローカルサーバー
* scssのコンパイル
* JSや画像の結合、圧縮
* ファイルの変更検知
* 各種ファイルのLint（コードチェック）

## クイックスタート

gulpコマンドのインストール

```bash
npm i -g gulp-cli
```

プロジェクトディレクトリに移動

```bash
cd <プロジェクトディレクトリ>
```

package.jsonの作成

```bash
npm init -y
```

Gulpおよび関連ツールのインストール

```bash
npm i gulp gulp-sass browser-sync gulp-imagemin gulp-plumber
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
gulp
```

このタスクではローカルサーバーの立ち上げ、sassのコンパイル、ファイルの変更検知を行なっています。gulpが起動するとターミナル、コマンドプロントは操作を受け付けなくなります。停止する場合は `Ctrl + c` を押してください。

## Tips

### 新たなパッケージの追加

新たなパッケージは `npm i -D <パッケージ名>` で追加できます。gulp起動中にパッケージを追加した場合、一度gulpタスクを停止し、再起動する必要があります。