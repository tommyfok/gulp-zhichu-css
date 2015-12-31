# gulp-zhichu-css

让引用的css直接输出成`<style>`形式，加快页面加载速度。

> CSS中引用的图片会转换成data-url的形式，如果转换失败，会尝试寻找文件对于html的相对路径，如果还是找不到，那就不做任何改动了。

## Installation
```
npm install -S gulp-zhichu-css
```

## Usage
```
var gulp = require('gulp');
var gzc = require('gulp-zhichu-css');

gulp.task('zhichu-css', function () {
  gulp.src('src/*.html')
    .pipe(gzc())
    .pipe(gulp.dest('./dist/'));
});
```
