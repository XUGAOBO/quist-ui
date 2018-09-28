# Dialog

> 弹出式提示框，有多种交互形式。


## 安装

```
$ npm install quist-ui -g
```

## 引入
```ux
<import name="quist-dialog" src="@quist-ui/quist-dialog/index"></import>
```

## 例子

#### 常规对话框

```ux
<quist-dialog mask-closable="{{true}}" title="标题" cancel-text="取消" @on-cancel="onCancel" @on-ok="onOk" content="这是内容这是内容" type="normal">
</quist-dialog>
```

#### 只有一个按钮的对话框

```ux
<quist-dialog mask-closable @on-cancel="onCancel" title="标题" @on-ok="onOk" content="只有一个确定按钮" type="onebtn">
</quist-dialog>
```

#### 无标题的对话框（点击蒙层不关闭弹窗）

```ux
<quist-dialog @on-cancel="onCancel" cancel-text="取消" @on-ok="onOk" content="没有标题没有标题没有标题没有标题没有标题" type="notitle">
</quist-dialog>
```

#### 无底部按钮无标题的对话框

```ux
<quist-dialog mask-closable="{{true}}" footer="{{false}}" @on-cancel="onCancel" content="没有标题没有标题没有标题没有标题没有标题" type="nofooter">
</quist-dialog>
```

更详细代码可以参考 [quist-dialog demo](https://github.com/qapp-ui/qapp-ui/blob/master/src/Button/index.ux)

## API 

| 属性 | 说明 | 类型 | 默认值 |
|-------------|------------|:--------:|:-----:|
| maskClosable | 点击蒙层是否允许关闭 | `Boolean` | false |
| visible | 对话框是否可见 | `Boolean` | false |
| title | 标题（如果不想显示标题，请不要传此参数） | `String` | - |
| content | 内容 | `String` | - |
| ok-text | 确认按钮文案 | `String` | 确定 |
| cancel-text | 取消按钮文案（如果只想显示一个按钮，请不要传此参数） | `String` | - |
| type | 弹窗类型，可选值为 `normal` `onebtn` `notitle` | `String` | - |
| footer | 底部两个按钮是否都显示 | `Boolean` | true |
| on-cancel | 点击遮罩层或取消按钮的回调 | `Function` | - |
| on-ok | 点击确定按钮的回调 | `Function` | - |


## 更新日志

v1.0.0（2018-09-30）
> 初始版本
