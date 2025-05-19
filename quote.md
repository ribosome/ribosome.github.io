---
layout: default
title: 線上報價
---

<div class="container">
  <h1>線上報價</h1>
  <form action="https://formspree.io/f/xyyljqen" method="POST">
    <div class="input-field">
      <input id="name" type="text" name="name" required>
      <label for="name">姓名</label>
    </div>
    <div class="input-field">
      <input id="email" type="email" name="email" required>
      <label for="email">Email</label>
    </div>
    <div class="input-field">
      <input id="phone" type="text" name="phone">
      <label for="phone">電話</label>
    </div>
    <div class="input-field">
      <textarea id="details" class="materialize-textarea" name="details"></textarea>
      <label for="details">需求描述</label>
    </div>
    <button type="submit" class="btn waves-effect">送出</button>
  </form>
</div>
