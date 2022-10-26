# 甜糖自动脚本

## 支持以下功能：
1. 新版本API账号登录（截止2022.10.26有效）
2. 自动签到
3. 自动收取星愿

## 使用方法：
1. 将token和signin放在同一个目录下，如/root下，linux上需要执行以下命令设置运行权限  
   chmod +x token signin
2. 运行token命令登录，按照提示输入手机号和短信验证码  
   备注：甜糖官方开启了图形验证码登录，我的程序中自动调用OCR识别验证码，有一定几率识别错误，登录失败了多试几次即可。注意不要太频繁重试，会被甜糖官方封锁
3. 如果上一步提示成功，会在当前目录生成token.txt，此文件即为后续自动操作的登录凭证，不可删除
4. 将signin加入任务计划中，每日定时执行一次即可  
   如在linux中，以root身份运行以下命令即可设置每日03：45自动签到和收星  
   echo "45 3 * * * root /root/signin" >> /etc/crontab
5. 如果哪天发现自动签到没执行，说明token失效了，重新登录即可


### 如果本项目对你有帮助，请在甜糖APP中填入作者的邀请码004347支持一下作者，并可以获得15张收益加速卡


如果对本项目有什么问题，可以联系作者邮箱axiang117@hotmail.com