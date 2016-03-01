#astros-css-less2

astros的插件，支持LESS解析。

针对原生LESS语法，新增__@include__关键字，表示引用cssLib根目录文件。


```
--[dir]projectRoot
    --[dir]assets
        --[dir]cssLib
            --【dir】base
                --[file]reset.less
            --[file]document.less
    --[dir]pages
        --[dir]index
            --[file]index.html
            --[file]index.less
                @include "document"

```

`pages/index/index.less`引用了 `assets/cssLib/document.less`,在`document.less`中，要引用reset，可使用以下语法

语法1

```
@include "base/reset"
```

语法2

```
@import ./base/reset
```

