---
id: cdn-links
title: CDN সংযোজকসমূহ 
permalink: docs/cdn-links.html
prev: create-a-new-react-app.html
next: release-channels.html
---

React এবং ReactDOM উভয়ই CDN-এ পাওয়া যাবে।

```html
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
```

উপরের সংস্করণগুলো কেবল বিকাশনের জন্যে নির্দেশিত, উৎপাদনের জন্যে উপযুক্ত নয়। React এর সংক্ষিপ্ত এবং নিখুঁত উৎপাদনীয় সংস্করণ এখানে পাওয়া যাবেঃ

```html
<script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
```

`react` এবং `react-dom` এর নির্দিষ্ট ভার্সন পেতে, `18` এর স্থানে অন্য ভার্সন সংখ্যা প্রতিস্থাপন করুন।

### `crossorigin` অ্যাট্রিবিউটটি কেন? {#why-the-crossorigin-attribute}

আপনি যদি একটি CDN থেকে React পরিবেশন করে থাকেন, তবে আমরা [`crossorigin`](https://developer.mozilla.org/en-US/docs/Web/HTML/CORS_settings_attributes) অ্যাট্রিবিউটটি রাখার পরামর্শ দিচ্ছিঃ

```html
<script crossorigin src="..."></script>
```

আমরা আরো সুপারিশ করি যে, আপনি যে CDN ব্যবহার করছেন ওটাতে `Access-Control-Allow-Origin: *` HTTP হেডার আছে কি তা যাচাই করে দেখতেঃ

![Access-Control-Allow-Origin: *](../images/docs/cdn-cors-header.png)

এটা React 16 এবং এর পরবর্তী সংস্করণগুলোতে আরো ভালো [ইরর হ্যান্ডেল করার অভিজ্ঞতা](/blog/2017/07/26/error-handling-in-react-16.html) দেয়।
