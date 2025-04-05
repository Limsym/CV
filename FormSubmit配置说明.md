# FormSubmit 配置说明

## 如何让联系表单正常工作

您的简历网页现在已经集成了FormSubmit服务，这是一个免费的表单处理服务，可以将表单提交内容通过电子邮箱发送给您。要使其正常工作，请按照以下步骤操作：

### 1. 替换您的电子邮箱

在`index.html`文件中，找到以下代码行：

```html
<form id="contactForm" class="space-y-4" aria-labelledby="contact-form-heading" action="https://formsubmit.co/your.email@example.com" method="POST">
```

将`your.email@example.com`替换为您的实际电子邮箱地址。

### 2. 首次使用激活

当有人第一次提交表单时，FormSubmit会向您的邮箱发送一封确认邮件。您需要点击邮件中的激活链接来确认您的电子邮箱地址。这是一次性的操作，之后所有的表单提交都会直接发送到您的邮箱。

### 3. 自定义选项（可选）

您可以根据需要调整以下配置选项：

- `_subject`: 邮件主题，当前设置为"简历网页的新消息"
- `_captcha`: 是否启用验证码，当前设置为false（不启用）
- `_next`: 提交成功后重定向的URL，当前为空（留在当前页面）
- `_template`: 邮件模板，当前设置为"table"（表格形式）
- `_autoresponse`: 自动回复消息，当前设置为"感谢您的留言，我会尽快回复您。"

如果您想在表单提交后重定向到特定页面，可以创建一个感谢页面（如thanks.html），然后更新`_next`参数的值。

### 4. 高级功能

FormSubmit还提供其他高级功能，如文件上传、自定义重定向、Webhook集成等。如需了解更多信息，请访问[FormSubmit官方网站](https://formsubmit.co/)。

## 注意事项

1. FormSubmit的免费版本每月有提交次数限制，对于个人简历网站通常足够使用。
2. 如果您收到垃圾邮件，可以启用验证码功能（将`_captcha`设置为true）。
3. 确保您提供的电子邮箱正确且可以正常接收邮件。
4. 定期检查垃圾邮件文件夹，以防表单提交通知被误归类。

## 故障排除

如果表单不能正常工作：

1. 确认您已经替换了正确的电子邮箱地址
2. 检查您是否已经点击了激活邮件中的确认链接
3. 确保您的网站可以正常访问外部服务（如FormSubmit）
4. 检查浏览器控制台是否有任何错误信息

如需更多帮助，请访问[FormSubmit帮助中心](https://formsubmit.co/help)。