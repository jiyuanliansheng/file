# 完美解决 fatal: unable to access ‘https://github.com/.../.git‘: Could not resolve host: github.com



**简介：** 完美解决 fatal: unable to access ‘https://github.com/.../.git‘: Could not resolve host: github.com

只需要在命令行中执行

```
git config --global --unset http.proxy 
git config --global --unset https.proxy

解决方案：cmd下命令执行 ipconfig/flushdns
清理dns缓存
```