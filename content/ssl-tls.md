从数字签名到https
https://www.ruanyifeng.com/blog/2011/08/what_is_a_digital_signature.html
https://www.ruanyifeng.com/blog/2014/02/ssl_tls.html
https://www.jianshu.com/p/4cf92c5a386d
https://www.jianshu.com/p/46e48bc517d0
https://cloud.tencent.com/developer/article/1458151
https://laravelacademy.org/post/21040
https://blog.51cto.com/tchuairen/1782945
https://blog.fundebug.com/2019/09/17/mitm-for-https/
证书链补全 https://www.gworg.com/problems/834.html

ca签名证书的两个作用，证明服务器的身份可信，加密信息。
客户浏览器检查服务器送过来的证书是否是由自己信赖的CA中心所签发的。如果是，就继续执行协议；如果不是，客户浏览器就给客户一个警告消息：警告客户这个证书不是可以信赖的询问客户是否需要继续。
自签名证书无法证明身份，可以用于加密信息。