# DISCLAMER
All work credit to [the original Yunzai-Bot](https://github.com/Le-niao/Yunzai-Bot)

# fork 说明
1. 本分支将原 Yunzai 使用的 oicq 迁移到为目前在频繁更新维护的 icqq，以解决因为手 Q 协议更新而导致在登录时出现的诸如 “版本过低，禁止登录” 一类的问题

2. 因为使用的是 npm alias 的方法将 oicq 移花接木到 icqq 上， 所以针对原版 Yunzai-Bot 开发的插件从原理上应该可以无痛迁移到本分支中 （实测 miao-plugin 无需作出任何更改）

3. 值得注意的是，因为 oicq 和 icqq 的设备信息写法不同，device.json 和 token 无法与原版 Yunzai-Bot 通用。因此第一次使用本分支前，请务必重新使用 ```pnpm run login``` 执行登录操作

4. 第一次以后台值守方式启动前请先执行 ```pnpm pm2 delete Yunzai-Bot```， 然后再执行 ```pnpm run start``` 启动，否则 PM2 可能执行的还是原版 Yunzai-Bot 而不是当下这个新的分支（本人笨b踩过这个坑两回）

5. ```device.json``` 的存放路径不再是原版 Yunzai-Bot 的 ```data/${uin}/device-${uin}.json```，而是 ```data/device.json```，token 文件存放路径同上

# Yunzai-Bot v3
云崽v3.0，原神qq群机器人，通过米游社接口，查询原神游戏信息，快速生成图片返回

项目仅供学习交流使用，严禁用于任何商业用途和非法行为

[目前功能](https://github.com/Le-niao/Yunzai-Bot/tree/main/plugins/genshin)

## 使用方法
>环境准备： Windows or Linux，Node.js（[版本至少v16以上](http://nodejs.cn/download/)），[Redis](https://redis.io/docs/getting-started/installation/)

1.克隆项目
```
git clone --depth=1 -b main https://github.com/Le-niao/Yunzai-Bot.git
```
```
cd Yunzai-Bot #进入Yunzai目录
```
2.安装[pnpm](https://pnpm.io/zh/installation)，已安装的可以跳过
```
npm install pnpm -g
```
3.安装依赖
```
pnpm install -P
```
4.运行（首次运行按提示输入登录）
```
node app
```

## 致谢
| Nickname                                                     | Contribution                        |
| :----------------------------------------------------------: | ----------------------------------- |
|[GardenHamster](https://github.com/GardenHamster/GenshinPray) | 模拟抽卡背景素材来源 |
|[西风驿站](https://bbs.mihoyo.com/ys/collection/839181) | 角色攻略图来源 |
|[米游社友人A](https://bbs.mihoyo.com/ys/collection/428421) | 角色突破素材图来源 |

## 其他
- 最后给个star或者[爱发电](https://afdian.net/@Le-niao)，你的支持是维护本项目的动力~~
- 图片素材来源于网络，仅供交流学习使用
- 严禁用于任何商业用途和非法行为
