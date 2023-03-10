# Day0

這所有的一切根本，就從寫網頁前端開始，從學習 CSS 框架開始，Tailwind CSS 是一個簡單且易學的框架，只要有瞭解基本的 HTML 語法就可以開始了。



### Bootstrap 與 Tailwind CSS

Tailwind CSS 是一個 CSS 框架，而這個框架跟 Bootstrap 有什麼差別，Bootstrap 用得好好的，我們還需要一個新的 CSS 框架嗎？直接來比較兩者的使用差別。



如果要使用 Bootstrap 來製作一個按鈕，會直接寫：

```html
<button type="button" class="btn btn-primary">Primary</button>
```



那如果改用 Tailwind CSS ，要製作一個按鈕時，會發現官方並沒有提供按鈕的元件來直接使用，而是任意由自己來定義，所以如果使用 Tailwind CSS 來製作按鈕時，可能會這樣寫：

```html
<a class="rounded border border-black bg-blue-500 px-12 py-3 text-lg text-white hover:bg-transparent hover:text-indigo-600" href="/">Button</a>
```



兩者的差別顯而易見，Tailwind CSS 用了許多類別才能製作一個按鈕，而 Bootstrap 只需要兩個 class 就搞定了，但必要因此就說 Bootstrap 比 Tailwind CSS 好用且簡單，事情並不是表面上看到的這個樣子。



先來看看 Bootstrap 的原始檔案是如何定義 btn 這個類別的：

```css
.btn {
  --bs-btn-padding-x: 0.75rem;
  --bs-btn-padding-y: 0.375rem;
  --bs-btn-font-family: ;
  /* ...省略 */
  display: inline-block;
  padding: var(--bs-btn-padding-y) var(--bs-btn-padding-x);
  font-family: var(--bs-btn-font-family);
  font-size: var(--bs-btn-font-size);
  font-weight: var(--bs-btn-font-weight);
  line-height: var(--bs-btn-line-height);
  /* ...省略 */
}
```

會發現 Bootstrap 直接把一個按鈕的樣式通通定義在 btn 裏面，好處是使用方便，直接兩個類別就可以引用到 HTML 檔案，但缺點是修改不易，如果只是想要修改字形的大小也是非常不容易的。



那麼 Tailwind CSS 在製作按鈕上，用了許多類別，直接觀看原始的 CSS 檔案：

```css
.rounded {
  border-radius: 0.25rem;
}

.border {
  border-width: 1px;
}

.px-12 {
  padding-left: 3rem;
  padding-right: 3rem;
}
```

會發現在 Tailwind CSS 上每一種 class 就專心定義一件事情而已，如圓角就定義圓角，寬度就定義寬度，而且可以直接從命名上清楚知道該 class 大概會是什麼樣式。反觀 Bootstrap ，卻無法知道 btn 這個 class 的詳細定義，只能知道它是按鈕元件。



所以 Tailwind CSS 才又稱為 utility-first CSS 框架，功能優先的 CSS 框架，也就是一個 class 只負責單一性的樣式呈現，看到名稱就可以知道效果。而 Bootstrap 稱為 Components 框架，組件框架。



### 如何選擇這兩個框架

Tailwind CSS 框架，使用彈性大較大，在開發上比較可以做出自己想要的樣式卻又不想修改 CSS 的專案。而 Bootstrap 如果要做出想要的樣式就必須要修改 CSS，開發上並沒有比較省時間，而如果都用其提供好的元件，確實適合需要快速開發的專案。