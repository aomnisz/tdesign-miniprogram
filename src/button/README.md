---
title: Button 按钮
description: 用于开启一个闭环的操作任务，如“删除”对象、“购买”商品等。
spline: base
isComponent: true
---

<span class="coverages-badge" style="margin-right: 10px"><img src="https://img.shields.io/badge/coverages%3A%20lines-100%25-blue" /></span><span class="coverages-badge" style="margin-right: 10px"><img src="https://img.shields.io/badge/coverages%3A%20functions-100%25-blue" /></span><span class="coverages-badge" style="margin-right: 10px"><img src="https://img.shields.io/badge/coverages%3A%20statements-100%25-blue" /></span><span class="coverages-badge" style="margin-right: 10px"><img src="https://img.shields.io/badge/coverages%3A%20branches-83%25-blue" /></span>
## 引入

全局引入，在 miniprogram 根目录下的`app.json`中配置，局部引入，在需要引入的页面或组件的`index.json`中配置。

```json
"usingComponents": {
  "t-button": "tdesign-miniprogram/button/button",
  "t-button-group": "tdesign-miniprogram/button-group/button-group"
}
```

### 主题定制

CSS 变量名|说明
--|--
--td-button-default-color | 默认按钮文本颜色
--td-button-default-border-color | 默认按钮边框颜色
--td-button-default-bg-color | 默认按钮背景颜色
--td-button-default-disabled-color | 默认按钮禁用态颜色
--td-button-primary-color | 品牌按钮文本颜色
--td-button-primary-border-color | 品牌按钮边框颜色
--td-button-primary-bg-color | 品牌按钮背景颜色
--td-button-primary-disabled-color | 品牌按钮禁用态颜色
--td-button-danger-color | 危险按钮文本颜色
--td-button-danger-border-color | 危险按钮边框颜色
--td-button-danger-bg-color | 危险按钮背景颜色
--td-button-danger-disabled-color | 危险按钮禁用态颜色
--td-button-primary-outline-color | 品牌线框按钮文本和边框颜色
--td-button-primary-outline-disabled-color | 品牌线框按钮禁用态颜色
--td-button-danger-outline-color | 危险线框按钮文本和边框颜色
--td-button-danger-outline-disabled-color | 危险线框按钮禁用态颜色
--td-button-primary-dashed-color | 品牌点状框按钮文本和边框颜色
--td-button-primary-dashed-disabled-color | 品牌点状框按钮禁用态颜色
--td-button-danger-dashed-color | 危险点状框按钮文本和边框颜色
--td-button-danger-dashed-disabled-color | 危险点状框按钮禁用态颜色
--td-button-primary-text-color | 品牌文本框按钮文本颜色
--td-button-primary-text-disabled-color | 品牌文本框按钮文本禁用态颜色
--td-button-danger-text-color | 危险文本框按钮文本颜色
--td-button-danger-text-disabled-color | 危险文本框按钮文本禁用态颜色
--td-button-ghost-color | 幽灵按钮文本颜色
--td-button-ghost-border-color | 幽灵按钮边框颜色
--td-button-ghost-disabled-color | 幽灵按钮文本禁用态颜色

## 代码演示

### 基础按钮

<img src="https://tdesign.gtimg.com/miniprogram/readme/button-1.png" width="375px" height="50%">
基础类型分为主按钮、次按钮、文字按钮

#### 次按钮
使用场景：在用户进行的操作为流程中的辅助操作，或者进行不那么重要的交互行为时，选择用次按钮；次要按钮通常和主要按钮一起出现

#### 主按钮
使用场景：大部分场景都可以使用，例如反馈页、表单页、对话框，一个页面建议最多只出现一个主按钮；

#### 文字按钮
使用场景：它的操作通常和其旁边内容相关，通常出现在标题旁、字段旁、列表最下方

{{ base }}

### 带图标按钮
{{ icon-btn }}

### 不同尺寸

{{ size }}

## API
### Button Props

名称 | 类型 | 默认值 | 说明 | 必传
-- | -- | -- | -- | --
block | Boolean | false | 是否为块级元素 | N
content | String / Slot | - | 按钮内容 | N
custom-dataset | Object | - | 自定义 dataset，可通过 event.currentTarget.dataset.custom 获取。TS 类型：`any` | N
custom-style `v0.25.0` | String | - | 自定义组件样式 | N
disabled | Boolean | false | 禁用状态 | N
external-classes | Array | - | 组件类名。`['t-class', 't-class-icon', 't-class-loading']` | N
ghost | Boolean | false | 是否为幽灵按钮（镂空按钮） | N
icon | String | - | 图标名称 | N
icon-props | Object | {} | 图标属性，透传至 icon | N
loading | Boolean | false | 是否显示为加载状态 | N
loading-props | Object | - | 加载loading样式。TS 类型：`LoadingProps`，[Loading API Documents](./loading?tab=api)。[详细类型定义](https://github.com/Tencent/tdesign-miniprogram/tree/develop/src/button/type.ts) | N
shape | String | rectangle | 按钮形状，有 4 种：长方形、正方形、圆角长方形、圆形。可选项：rectangle/square/round/circle | N
size | String | medium | 组件尺寸。可选项：small/medium/large。TS 类型：`SizeEnum` | N
theme | String | default | 组件风格，依次为品牌色、危险色。可选项：default/primary/danger | N
type | String | - | 同小程序的 formType。可选项：submit/reset | N
variant | String | base | 按钮形式，基础、线框、文字。可选项：base/outline/dashed/text | N
open-type | String | - | 微信开放能力。<br />具体释义：<br />`contact` 打开客服会话，如果用户在会话中点击消息卡片后返回小程序，可以从 bindcontact 回调中获得具体信息，<a href="https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/customer-message/customer-message.html">具体说明</a> （*小程序插件中不能使用*）；<br />`share` 触发用户转发，使用前建议先阅读<a href="https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/share.html#使用指引">使用指引</a>；<br />`getPhoneNumber` 获取用户手机号，可以从 bindgetphonenumber 回调中获取到用户信息，<a href="https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/getPhoneNumber.html">具体说明</a> （*小程序插件中不能使用*）；<br />`getUserInfo` 获取用户信息，可以从 bindgetuserinfo 回调中获取到用户信息 （*小程序插件中不能使用*）；<br />`launchApp` 打开APP，可以通过 app-parameter 属性设定向 APP 传的参数<a href="https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/launchApp.html">具体说明</a>；<br />`openSetting` 打开授权设置页；<br />`feedback` 打开“意见反馈”页面，用户可提交反馈内容并上传<a href="https://developers.weixin.qq.com/miniprogram/dev/api/base/debug/wx.getLogManager.html">日志</a>，开发者可以登录<a href="https://mp.weixin.qq.com/">小程序管理后台</a>后进入左侧菜单“客服反馈”页面获取到反馈内容；<br />`chooseAvatar` 获取用户头像，可以从 bindchooseavatar 回调中获取到头像信息。<br />[小程序官方文档](https://developers.weixin.qq.com/miniprogram/dev/component/button.html)。可选项：contact/share/getPhoneNumber/getUserInfo/launchApp/openSetting/feedback/chooseAvatar | N
hover-stop-propagation | Boolean | false | 指定是否阻止本节点的祖先节点出现点击态 | N
hover-start-time | Number | 20 | 按住后多久出现点击态，单位毫秒 | N
hover-stay-time | Number | 70 | 手指松开后点击态保留时间，单位毫秒 | N
lang | String | en | 指定返回用户信息的语言，zh_CN 简体中文，zh_TW 繁体中文，en 英文。。<br />具体释义：<br />`en` 英文；<br />`zh_CN` 简体中文；<br />`zh_TW` 繁体中文。<br />[小程序官方文档](https://developers.weixin.qq.com/miniprogram/dev/component/button.html)。可选项：en/zh_CN/zh_TW | N
session-from | String | - | 会话来源，open-type="contact"时有效 | N
send-message-title | String | 当前标题 | 会话内消息卡片标题，open-type="contact"时有效 | N
send-message-path | String | 当前分享路径 | 会话内消息卡片点击跳转小程序路径，open-type="contact"时有效 | N
send-message-img | String | 截图 | 会话内消息卡片图片，open-type="contact"时有效 | N
app-parameter | String | - | 打开 APP 时，向 APP 传递的参数，open-type=launchApp时有效 | N
show-message-card | Boolean | false | 是否显示会话内消息卡片，设置此参数为 true，用户进入客服会话会在右下角显示"可能要发送的小程序"提示，用户点击后可以快速发送小程序消息，open-type="contact"时有效 | N
bindgetuserinfo | Eventhandle | - | 用户点击该按钮时，会返回获取到的用户信息，回调的 detail 数据与<a href="https://developers.weixin.qq.com/miniprogram/dev/api/open-api/user-info/wx.getUserInfo.html">wx.getUserInfo</a>返回的一致，open-type="getUserInfo"时有效 | N
bindcontact | Eventhandle | - | 客服消息回调，open-type="contact"时有效 | N
bindgetphonenumber | Eventhandle | - | 获取用户手机号回调，open-type=getPhoneNumber时有效 | N
binderror | Eventhandle | - | 当使用开放能力时，发生错误的回调，open-type=launchApp时有效 | N
bindopensetting | Eventhandle | - | 在打开授权设置页后回调，open-type=openSetting时有效 | N
bindlaunchapp | Eventhandle | - | 打开 APP 成功的回调，open-type=launchApp时有效 | N
bindchooseavatar | Eventhandle | - | 获取用户头像回调，open-type=chooseAvatar时有效 | N

### Button Events

名称 | 参数 | 描述
-- | -- | --
tap | `event` | 点击时触发
