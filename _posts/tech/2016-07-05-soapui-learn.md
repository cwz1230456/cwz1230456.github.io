---
layout: post
title: soapui学习总结
category: 技术
tags: soapui
keywords: soapui,学习
description: 
---

# soapui学习总结

> 学习soapui，对业财绩校协同平台进行WebServices接口进行测试（与SAP连接的接口）

## Soapui简要操作
  功能测试：导航面板New SoapUi Project ——> 导入WSDL文件 ——> 保存 ——> 生成测试包（如果需要导入，选Import Project）
  
  用例创建：test steps ——> 请求编辑器
  
  断言功能
  
  负载测试：相较于LoadRunner，SoapUI根据WSDL文件生成soap数据包，填入参数即可测试，且拥有数据监控和图表，但是LoadRunner的通标更丰富精准

具体参照如下两篇文章：

http://www.open-open.com/doc/view/2cabd58c5da341fc8aaf1cda13f2c6c5

http://wenku.baidu.com/link?url=g3LUEFm-L88-s4XoL_v7rrzgnGW0U-CuvHLLkUCkVojLLBKUggvTAtCtS8BMdOj_vm2FVg__03_5A-x5Pr_Cnpj7sk_iQQFV0-SnQWeP1yS

## Soapui相关知识总结
