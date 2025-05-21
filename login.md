---
layout: default
title: 會員登入
---

<div class="container">
  <h1>會員登入</h1>
  <form action="#" method="POST">
    <div class="input-field">
      <input id="email" type="email" name="email" required>
      <label for="email">Email</label>
    </div>
    <div class="input-field">
      <input id="password" type="password" name="password" required>
      <label for="password">密碼</label>
    </div>
    <button type="submit" class="btn waves-effect">登入</button>
    <button id="corp-cert-login" type="button" class="btn waves-effect" style="margin-left: 1rem;">工商憑證登入</button>
  </form>
  <div id="cert-modal" class="modal">
    <div class="modal-content">
      <h4>工商憑證資訊</h4>
      <pre id="cert-data"></pre>
    </div>
    <div class="modal-footer">
      <a href="#!" class="modal-close waves-effect btn-flat">關閉</a>
    </div>
  </div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    var btn = document.getElementById('corp-cert-login');
    var modalElem = document.getElementById('cert-modal');
    var certDataElem = document.getElementById('cert-data');
    if (btn) {
      btn.addEventListener('click', function() {
        fetch('http://127.0.0.1:61161/pkcs11info?withcert=true')
          .then(function(resp) { return resp.text(); })
          .then(function(text) {
            if (certDataElem) {
              certDataElem.textContent = text;
            }
            var instance = M.Modal.getInstance(modalElem);
            instance.open();
          })
          .catch(function(err) {
            if (certDataElem) {
              certDataElem.textContent = '無法取得憑證資訊';
            }
            var instance = M.Modal.getInstance(modalElem);
            instance.open();
          });
      });
    }
  });
</script>
