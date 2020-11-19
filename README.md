## 1.下载
github上下载：[https://github.com/Dreamacro/clash/releases/](https://github.com/Dreamacro/clash/releases/)
找一个linux 64位的比如：
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020111921101068.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3d4a2h0dXJmdW4=,size_16,color_FFFFFF,t_70#pic_center)下载并解压，将解压后的文件重命名为clash。

接着导出你的.yaml文件，这个文件是要供应商提供，需要资金支持
以下列出前几行
```bash
port: 7890
socks-port: 7891
redir-port: 7892
allow-lan: false
mode: Rule
log-level: silent
```
## 2.启动与配置
本人目前还没找到桌面图形化界面，唉，之后再说
首先增加下载的clash  for linux的权限
***1.启动：***
```bash
sudo chmod a+x clash
```
然后执行：

```bash
./clash
```
首次执行，会提示什么诸如
INFO[0000] Can't find MMDB, start download 
之类的东西，大概出来两三行，就不接着出现了，这时，停止执行clash :Ctrl + C
***2.配置：***

```bash
cd ~/.config/clash
ls
```
你会发现一个config.yaml的文件，将文件中的内容替换为你的.yaml文件的内容并保存。
之后配置网络见下图
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020111921312714.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3d4a2h0dXJmdW4=,size_16,color_FFFFFF,t_70#pic_right#pic_center)
最后重启你的电脑，重新运行clash

```bash
./clash
```
会出现看起来“正常”点的东西，这里不方便展示，注意，此处别关闭clash
然后打开网址：[http://clash.razord.top/#/proxies](http://clash.razord.top/#/proxies)进行相关配置即可
配置好后，可以关闭该页，此时你已可以科学上网。

<h1 align="center">
  <img src="https://user-images.githubusercontent.com/1166872/47954055-97e6cb80-dfc0-11e8-991f-230fd40481e5.png" alt="yacd">
</h1>

> Yet Another [Clash](https://github.com/Dreamacro/clash) [Dashboard](https://github.com/Dreamacro/clash-dashboard)

The site [http://yacd.haishan.me](http://yacd.haishan.me) is served with HTTP not HTTPS is because many browsers block requests to HTTP resources from a HTTPS website. If you think it's not safe, you could just download the [zip of the gh-pages](https://github.com/haishanh/yacd/archive/gh-pages.zip), unzip and open or serve `index.html` directly.

[Docker image](https://hub.docker.com/r/haishanh/yacd) is also available as `haishanh/yacd`.

## Development

```sh
# install dependencies
yarn

# start the dev server
# then go to http://127.0.0.1:3000
yarn start


# build optimized assets
# ready to deploy assets will be in the directory `public`
yarn build
```
