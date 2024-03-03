# V2ray for Doprax

#Introduction:

This project is used to deploy V2ray on Doprax.com free service. The solution adopted is Nginx + WebSocket + VMess/VLess + TLS. The speed is slower than Replit, but the official promotion is that there is no traffic limit and the service will never stop after it is started.

# Precautions:

<p><b><li>Please do not abuse, account ban will be at your own risk. </li></b></p>

<p><b><li>If you find that you cannot access the Internet after the deployment is completed, please check whether the domain name is blocked. You can use Cloudflare CDN to solve the problem. </li></b></p>

#deploy:

<p>1. Log in to your GitHub account and Fork the project. </p>

<p>2. Registration<a>

<a href="https://www.doprax.com/signup/">Doprax.com</a> Log in and import the project. </p>

<p>For detailed usage plan, please refer to: https://www.hicairo.com/post/55.html</p>

# Instructions:

<p>1. Server-side configuration</p>

<p>Please use <a href="https://www.v2fly.org/awesome/tools.html"> third-party tools</a> to generate a new UUID. After logging in to Doprax.com, click Main in the left menu, Edit source code on the right side of the window, select the Dockerfile file, edit the UUID and camouflage address information, save it and restart the service. </p>

<img src="[https://hicairo.com/zb_users/upload/2022/12/20221229167 2276227538571.webp](https://camo.githubusercontent.com/19968a471c92cc19cf6cc2c8909c8776d9ee44e0062c6fa5ec26387f434835e4/68747470733a2f2f6869636169726f2e636f6d2f7a625f75736572732f75706c6f61642f323032322f31322f3230323231323239313637323237363232373533383537312e77656270)">


<pre class="notranslate"><code># Replace de04add9-5c68-8bab-950c-08cd5320df18 with the newly generated UUID

ENV UUID de04add9-5c68-8bab-950c-08cd5320df18

# VMESS_WSPATH/VLESS_WSPATH two constants define Vmess/VLess respectively.

camouflage path,

#Please modify vmess or vless in the content respectively. Note: The camouflage path starts with the / symbol.

Necessary trouble, please do not use special symbols,

ENV VMESS_WSPATH/vmess

ENV VLESS_WSPATH /vless

</code></pre>

<p>2. Client configuration</p>

<p>Node client configuration needs to be done manually. The following takes V2rayN as an example.

<p>The picture below is a schematic diagram of VMess configuration. Please modify the label content. Other settings are consistent with those shown in the picture.

</p>

<img src="https://www.hicairo.com/zb_users/upload/2022/12/2022122 91672276258394161.webp">

<p>The picture below is a schematic diagram of VLess configuration. Please modify the label content. Other settings are consistent with those shown in the picture. </p>

<img src="https://www.hicairo.com/zb_users/upload/2022/12/2022122 91672276274474231.webp">
