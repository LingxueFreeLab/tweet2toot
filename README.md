# tweet2toot

A simple script that transport tweets from twitter to Mastodon. Based on the Twitter RSS feed powered by [RSSHub](https://rsshub.app).

```
pip3 install -r requirements.txt
cp conf.sample.ini conf.ini
nano conf.ini
python3 run.py
```

crontab job setting:
```
crontab -e
```
or (Ubuntu 18.04)
```
nano /etc/crontab
/etc/init.d/cron restart
```

Recommand do job hourly:
```
#m h dom mon dow user  command
13 *    * * *   root    cd /tweet2toot && python3 run.py
```

一个将推特搬运到长毛象的脚本——基于[RSSHub](https://rsshub.app)生成的推特RSS。

推特的开发者账号很长时间没有申请到，所以只能暂时用RSSHub作为数据源了。😢