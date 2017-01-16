# `<input type="password">`

- http://insecure.stzky.com/password/

Google Chrome 56以降ではHTTPS通信以外で`<input type="password">`を含むHTML文書を開いた際、ロケーションバーに「<q>保護されていない通信</q>」と表示されるようになります。

[![Google Chrome 56で`<input type="password">`を含むHTML文書を開いたときのロケーションバーの様子](screenshot.png)](screenshot.png)

HTTP通信では中間者攻撃によってHTML文書が改竄されてしまっている場合があります。HTML文書に改竄がある場合、攻撃者によってパスワードの詐取が行われてしまうおそれがあります。ログインフォームなど、パスワードの入力が発生するHTML文書ではHTTPS通信を用いた配信を行うべきでしょう。
