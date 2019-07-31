# css 实现进度条的功能

重点：

```scss
background-image: linear-gradient(to right top, green 50%, #fff 50%);
background-size: 100% calc(100% - 100vh + 5px);
```

上面的`5px`表示滚动条的宽度，`100vh`表示屏幕的高度。

```scss
body{
    position: relative;
    padding: 50px;
    font-size: 24px;
    line-height: 30px;
    background-image: linear-gradient(to right top, green 50%, #fff 50%);
    background-size: 100% calc(100% - 100vh + 5px);
    background-repeat: no-repeat;
    z-index: 1;
}
body::after {
    content: "";
    position: fixed;
    top: 5px;
    left: 0;
    bottom: 0;
    right: 0;
    background: #fff;
    z-index: -1;
}
```