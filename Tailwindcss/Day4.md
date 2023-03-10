# Day4

容器



#### Container

一個最基本的容器，使用 container，它的最大寬度為螢幕寬度，如螢幕尺寸縮小到 640 以下，就會呈現滿版：

```html
<div class="container mx-auto bg-slate-100">
  <div>Hello Tailwindcss</div>
</div>
```



#### 響應式排版容器

總共有 5 種螢幕尺寸表示：

- sm：640px
- md：768px
- lg：1024px
- xl：1280px
- 2xl：1536px



所以 container 加上響應式排版：

```html
<div class="container mx-auto bg-slate-100 sm:max-w-sm">
  <div>Hello Tailwindcss</div>
</div>
```

表示當螢幕尺寸大於 sm 時，也就是 640px 時，會將寬度設定為 max-w-sm。小於 640px時，會將寬度設定為 container。



針對不同尺寸定義寬度：

```html
<div class="container mx-auto bg-slate-100 sm:max-w-sm md:max-w-md lg:max-w-lg">
  <div>Hello Tailwindcss</div>
</div>
```

表示當螢幕尺寸大於 sm 且小於 md 時，也就是 640px ~ 768px 時，會將寬度設定為 max-w-sm。小於 640px 時，會將寬度設定為 container。螢幕尺寸大於 md 且小於 lg 時，也就是 768px ~ 1024px 時，會將寬度設定為 max-w-md。
