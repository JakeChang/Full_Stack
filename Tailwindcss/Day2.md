# Day2

Padding 與 Margin，留白屬性



### Padding

可以理解為內部留白，共有 6 種：

##### p

上下左右留白，留白 10：

```html
<div class="p-10">Hello Tailwindcss</div>
```



##### px

針對 x 軸，也就是左右留白，留白 10：

```html
<div class="px-10">Hello Tailwindcss</div>
```



##### py

針對 y 軸，也就是上下留白，留白 10：

```html
<div class="py-10">Hello Tailwindcss</div>
```



##### pt

只有上方留白，留白 10：

```html
<div class="pt-10">Hello Tailwindcss</div>
```



##### pr

只有右邊留白，留白 10：

```html
<div class="pr-10">Hello Tailwindcss</div>
```



##### pb

只有下方留白，留白 10：

```html
<div class="pb-10">Hello Tailwindcss</div>
```



##### pl

只有左邊留白，留白 10：

```html
<div class="pl-10">Hello Tailwindcss</div>
```





### Margin

與 Padding 相反，為外部留白，共有 6 種：

- m：上下左右留白
- mx：x軸，也就是左右留白
- my：y軸，也就是上下留白
- mt：只有上方留白
- mr：只有右邊留白
- mb：只有下方留白
- ml：只有左邊留白

後方帶入數字，就是表示要留白的大小為何，數字範圍從 0 ~ 96 不等



另外還有 6 種跟 auto 相關：

##### m-auto

上下左右留白大小一樣



##### mx-auto

針對 x 軸，也就是左右留白大小一樣，用來水平置中：

```html
<div class="mx-auto w-64 bg-blue-500">
  <p>Title</p>
</div>
```



##### my-auto

針對 y 軸，也就是上下留白大小一樣，用來垂直置中：

```html
<div class="flex h-screen">
  <div class="mx-auto my-auto w-64 bg-blue-500">Hello Tailwindcss</div>
</div>
```

也可以直接改寫成：

```html
<div class="flex h-screen">
  <div class="m-auto w-64 bg-blue-500">Hello Tailwindcss</div>
</div>
```



使用 my-auto 的情況通常是在內部元素的高度不固定時，需要讓其在垂直方向上置中。如果內部元素的高度已經是固定的，那麼使用 flex 和 justify-center items-center 這兩個 class 也可以達到水平和垂直置中的效果，而不需要使用 my-auto。

例如：

```html
<div class="flex h-screen items-center justify-center">
  <div class="h-64 w-64 bg-blue-500"></div>
</div>
```



##### mt-auto

針對上方留白，如果有固定高度的話，位置會完全靠下方：

```html
<div class="flex h-screen">
  <div class="mx-auto mt-auto h-64 w-64 bg-blue-500">Hello Tailwindcss</div>
</div>
```



##### mb-auto：

針對下方留白，如果有固定高度的話，位置會完全靠上方：

```html
<div class="flex h-screen">
  <div class="mx-auto mb-auto h-64 w-64 bg-blue-500">Hello Tailwindcss</div>
</div>
```



##### mr-auto：

只針對右邊留白，如果有固定寬度的話，位置會完全靠左邊：

```html
<div class="flex h-screen">
  <div class="mr-auto my-auto h-64 w-64 bg-blue-500">Hello Tailwindcss</div>
</div>
```



##### ml-auto：

只針對下方留白，如果有固定寬度的話，位置會完全靠右邊：

```html
<div class="flex h-screen">
  <div class="ml-auto my-auto h-64 w-64 bg-blue-500">Hello Tailwindcss</div>
</div>
```

