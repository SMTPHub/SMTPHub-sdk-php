# SMTPHub-SDK-PHP

## 使用方法：

```php
// 导入SDK
include('SMTPHub.php');
// 实例
$SMTP = new \lib\mail\SMTPHub('http://smtphub.yourcompany.com/api.php', APPID, APPSECRET);
// 调用发送接口
$SMTP->send('接收人邮箱', '主题', '内容', '收信人名字', '发信人名字');
```

实例

```php
// 导入SDK
include('SMTPHub.php');
// 实例
$SMTP = new \lib\mail\SMTPHub('http://smtphub.yourcompany.com/api.php', '1000', 'Cd2DBg2R0JuXgLsrkXb6AfLXV8kW8p4k');
// 定义参数
$to        = 'username@qq.com';
$to_name   = '接收人名字';
$subject   = "这是一封测试邮件";
$message   = "邮件内容";
$from_name = '发信人名字';
// 调用发送接口
$result    = $SMTP->send($to, $subject, $message, $to_name, $from_name);
// 输出结果
@header('Content-Type: application/json; charset=UTF-8');
echo $result;
```
