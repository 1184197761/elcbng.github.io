---
layout: note
title: 第三周学习笔记
author: 吴文展
category: 2020暑假第三周
date: 2020-08-02
---


## 学习内容：
* 使用CSS进行网页布局
* JavaScript进阶
* Dom事件处理
    * 实例：QQ界面、抽奖系统

## 学习体会：
* CSS个人感觉挺繁琐的，而且有点浪费时间，我更愿意套用别人的模板然后做一点修改。。。这可能是因为我经验不足，毕竟也没怎么写过网页。
* JavaScript之前学习三件套的时候有涉猎过，不过只学了基础所以没什么印象。这周学习了进阶的知识，发现其实挺有趣的，相比用CSS做动效我觉得js更加友好一点。。。
* Dom事件处理没有很深入的学习，主要了解了冒泡事件的机制，之后在制作QQ界面里面就用到了这个知识点。
* 今天才发现其他方向的还没碰，所以暂时只能提交一个作业，下周准备学习网络安全。

## 前端作业：
* 入门：
    * 页面：[QQ登录界面](../wz.html)
    * 笔记：见js文件
    
* 基础：
  
  ```css
  @media (max-width: 767px) {
      .custom-checkbox /*. 类选择器*/
          .custom-control-input:disabled:checked /*: 伪类选择器，选择被禁用且被选中的元素*/
          ~ .custom-control-label::before, /*~&:: 通用兄弟选择器+伪元素选择器，在元素前的一个插入元素*/
      /*上述选择的元素为（如果有）：custom-checkbox类下的两个任意位置子元素（input在前）*/
      .custom-checkbox
          .custom-control-input:disabled:checked::before,
      /*上述选择的结果为：custom-checkbox类下的被禁用且被选中的.custom-control-input元素的前一个插入元素*/
      .custom-checkbox
          .custom-control-input:disabled:indeterminate /*:indeterminate 选择状态不确定的元素（没搞懂）*/
          ~ .custom-control-label::before {
              background-color: #007bff; /*设置背景色*/
              animation: spining 4s linear infinite; /*设置动画（具体不清楚）*/
              width: 1vw; /*设置宽度为一个视口单位*/
              margin: 1rem; /*设置外边距为一个字体大小（相对于html的字体）*/
      }
  }
  ```
    没学过CSS3，所以参考了w3school和MDN的一些教程。至于《JavaScript高级程序设计》目前还没开始读，所以也没有相应的学习笔记。