# Day3

寬度與高度



### 寬度

寬度的表示式為 ```w-```，後方帶入 0 ~ 96 的範圍內的數值

例如：

```html
<div class="w-48 bg-slate-200">Hello Tailwindcss</div>
```

bg-slate-200 為灰色背景



另外也可以使用佔比百分比，例如 50%：

```html
<div class="w-1/2 bg-slate-200">Hello Tailwindcss</div>
```



其他幾個特殊的寬度：

##### w-full

根據父元素的最大寬度來顯示：

```html
<div class="w-1/2 bg-gray-300 p-4">
  <div class="w-full h-20 bg-red-500">Hello Tailwindcss</div>
</div>
```



##### w-screen

不管父元素的寬度，都使用螢幕的最大寬度來顯示

```html
<div class="w-screen bg-gray-300 p-4"></div>
```



##### w-min

根據內容來使用最小的寬度：

```html
<div class="w-1/2 bg-gray-300 p-4">
  <div class="w-min h-20 bg-red-500">Hello Tailwindcss</div>
</div>
```



##### w-max

不管父元素的寬度，如果內容超過父元素，就會超出父元素的範圍：

```html
<div class="w-1/12 bg-gray-300 p-4">
  <div class="w-max h-20 bg-red-500">Hello Tailwindcss</div>
</div>
```



##### w-fit

根據內容來制定寬度：

```html
<div class="w-1/2 bg-gray-300 p-4">
  <div class="w-fit h-20 bg-red-500">Hello Tailwindcss</div>
</div>
```



##### w-auto

寬度會根據其內容的寬度自動調整，使用 w-auto 的情況通常是當元素內容的寬度不是固定的，且希望元素能夠根據內容的寬度來自適應調整寬度時使用。

如：

```html
<div class="w-1/2 bg-slate-100">
  <div class="w-auto bg-blue-500">Hello Tailwindcss</div>
</div>
```

使用 w-auto 的 div 元素預設仍會滿寬度展示。這是因為 w-auto class 只會讓元素的寬度根據其內容自動調整，而不會限制其寬度。只要加上 max-w-max 就可以使寬度最大為其內容的寬度：

```html
<div class="w-1/2 bg-slate-100">
  <div class="w-auto max-w-max bg-blue-500">Hello Tailwindcss</div>
</div>
```





### 高度

寬度的表示式為 ```h-```，後方帶入 0 ~ 96 的範圍內的數值

例如：

```html
<div class="h-48 bg-slate-200">Hello Tailwindcss</div>
```



另外也可以使用佔比百分比，例如 33%：

```html
<div class="h-screen">
  <div class="h-1/3 bg-slate-200">Hello Tailwindcss</div>
</div>
```

需要注意的是，使用 h-1/3 前，必須要確保其父元素的高度是已知的，否則 h-1/3 無法生效。



其他幾個特殊的寬度：

##### h-full

根據父元素的最大高度來顯示：

```html
<div class="h-screen bg-gray-300 p-4">
  <div class="h-full bg-red-500">Hello Tailwindcss</div>
</div>
```



##### h-screen

占滿螢幕高度：

```html
<div class="h-screen bg-gray-300 p-4"></div>
```



##### h-min



##### h-max



##### h-fit



##### h-auto

