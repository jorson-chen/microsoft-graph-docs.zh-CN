---
title: Microsoft Intune 中的设备配置
description: 使用 Microsoft Intune 设备配置工作负载管理你管理的所有设备上的设置和功能。
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: conceptualPageType
ms.openlocfilehash: 6f36290ba88245bb09440b6a528c1395bd19029a
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2020
ms.locfileid: "48041580"
---
# <a name="device-configuration-in-microsoft-intune"></a>Microsoft Intune 中的设备配置

命名空间：microsoft.graph

> **注意：** 使用 Microsoft Graph API 配置 Intune 控件和策略仍需要客户[正确许可](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) Intune 服务。

使用 Microsoft Intune 设备配置工作负载管理你管理的所有设备上的设置和功能。

以下 Graph 资源可用于在 Intune 中管理设备上的设置和功能：

- [Android 合规性策略](intune-deviceconfig-androidcompliancepolicy.md)
- [Android 自定义配置](intune-deviceconfig-androidcustomconfiguration.md)
- [Android 常规设备配置](intune-deviceconfig-androidgeneraldeviceconfiguration.md)
- [Android 所需密码类型](intune-deviceconfig-androidrequiredpasswordtype.md)
- [Android 工作配置文件符合性策略](intune-deviceconfig-androidworkprofilecompliancepolicy.md)
- [Android 工作配置文件跨配置文件数据共享类型](intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)
- [Android 工作配置文件自定义配置](intune-deviceconfig-androidworkprofilecustomconfiguration.md)
- [Android 工作配置文件默认应用权限策略类型](intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)
- [Android 工作配置文件常规设备配置](intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)
- [Android 工作配置文件所需的密码类型](intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)
- [应用列表项](intune-deviceconfig-applistitem.md)
- [应用列表类型](intune-deviceconfig-applisttype.md)
- [应用保险箱应用程序控制类型](intune-deviceconfig-applockerapplicationcontroltype.md)
- [Apple 设备功能配置基础](intune-deviceconfig-appledevicefeaturesconfigurationbase.md)
- [应用程序防护阻止剪贴板共享类型](intune-deviceconfig-applicationguardblockclipboardsharingtype.md)
- [应用程序 Guard Block 文件传输类型](intune-deviceconfig-applicationguardblockfiletransfertype.md)
- [自动更新模式](intune-deviceconfig-automaticupdatemode.md)
- [BitLocker 加密方法](intune-deviceconfig-bitlockerencryptionmethod.md)
- [BitLocker 可移动驱动器策略](intune-deviceconfig-bitlockerremovabledrivepolicy.md)
- [星期几](intune-deviceconfig-dayofweek.md)
- [Defender 云块级别类型](intune-deviceconfig-defendercloudblockleveltype.md)
- [Defender 检测到的恶意软件操作](intune-deviceconfig-defenderdetectedmalwareactions.md)
- [Defender 监视器文件活动](intune-deviceconfig-defendermonitorfileactivity.md)
- [Defender 示例提交提示](intune-deviceconfig-defenderpromptforsamplesubmission.md)
- [Defender 扫描类型](intune-deviceconfig-defenderscantype.md)
- [Defender 威胁操作](intune-deviceconfig-defenderthreataction.md)
- [设备合规性操作项](intune-deviceconfig-devicecomplianceactionitem.md)
- [设备合规性操作类型](intune-deviceconfig-devicecomplianceactiontype.md)
- [设备合规性设备概述](intune-deviceconfig-devicecompliancedeviceoverview.md)
- [设备合规性设备状态](intune-deviceconfig-devicecompliancedevicestatus.md)
- [设备合规性策略](intune-deviceconfig-devicecompliancepolicy.md)
- [设备合规性策略分配](intune-deviceconfig-devicecompliancepolicyassignment.md)
- [设备合规性策略设备状态摘要](intune-deviceconfig-devicecompliancepolicydevicestatesummary.md)
- [设备合规性策略设置状态](intune-deviceconfig-devicecompliancepolicysettingstate.md)
- [设备合规性策略设置状态摘要](intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)
- [适用于规则的设备合规性计划操作](intune-deviceconfig-devicecompliancescheduledactionforrule.md)
- [设备合规性设置状态](intune-deviceconfig-devicecompliancesettingstate.md)
- [设备合规性用户概述](intune-deviceconfig-devicecomplianceuseroverview.md)
- [设备合规性用户状态](intune-deviceconfig-devicecomplianceuserstatus.md)
- [设备配置](intune-deviceconfig-deviceconfiguration.md)
- [设备配置分配](intune-deviceconfig-deviceconfigurationassignment.md)
- [设备配置设备概述](intune-deviceconfig-deviceconfigurationdeviceoverview.md)
- [设备配置设备状态摘要](intune-deviceconfig-deviceconfigurationdevicestatesummary.md)
- [设备配置设备状态](intune-deviceconfig-deviceconfigurationdevicestatus.md)
- [设备配置设置状态](intune-deviceconfig-deviceconfigurationsettingstate.md)
- [设备配置用户概述](intune-deviceconfig-deviceconfigurationuseroverview.md)
- [设备配置用户状态](intune-deviceconfig-deviceconfigurationuserstatus.md)
- [设备管理设置](intune-deviceconfig-devicemanagementsettings.md)
- [设备威胁防护级别](intune-deviceconfig-devicethreatprotectionlevel.md)
- [诊断数据提交模式](intune-deviceconfig-diagnosticdatasubmissionmode.md)
- [Edge cookie 策略](intune-deviceconfig-edgecookiepolicy.md)
- [Edge 搜索引擎](intune-deviceconfig-edgesearchengine.md)
- [Edge 搜索引擎基准](intune-deviceconfig-edgesearchenginebase.md)
- [Edge 搜索引擎自定义](intune-deviceconfig-edgesearchenginecustom.md)
- [Edge 搜索引擎类型](intune-deviceconfig-edgesearchenginetype.md)
- [版本升级配置](intune-deviceconfig-editionupgradeconfiguration.md)
- [版本升级许可证类型](intune-deviceconfig-editionupgradelicensetype.md)
- [防火墙证书吊销列表检查方法类型](intune-deviceconfig-firewallcertificaterevocationlistcheckmethodtype.md)
- [防火墙数据包排入队列方法类型](intune-deviceconfig-firewallpacketqueueingmethodtype.md)
- [防火墙预共享的密钥编码方法类型](intune-deviceconfig-firewallpresharedkeyencodingmethodtype.md)
- [Internet 站点安全级别](intune-deviceconfig-internetsitesecuritylevel.md)
- [iOS 证书配置文件](intune-deviceconfig-ioscertificateprofile.md)
- [iOS 合规性策略](intune-deviceconfig-ioscompliancepolicy.md)
- [iOS 自定义配置](intune-deviceconfig-ioscustomconfiguration.md)
- [iOS 设备功能配置](intune-deviceconfig-iosdevicefeaturesconfiguration.md)
- [iOS 常规设备配置](intune-deviceconfig-iosgeneraldeviceconfiguration.md)
- [iOS 主屏幕应用](intune-deviceconfig-ioshomescreenapp.md)
- [iOS 主屏幕文件夹](intune-deviceconfig-ioshomescreenfolder.md)
- [iOS 主屏幕文件夹页](intune-deviceconfig-ioshomescreenfolderpage.md)
- [iOS 主屏幕项](intune-deviceconfig-ioshomescreenitem.md)
- [iOS 主屏幕页](intune-deviceconfig-ioshomescreenpage.md)
- [iOS 网络使用规则](intune-deviceconfig-iosnetworkusagerule.md)
- [iOS 通知警报类型](intune-deviceconfig-iosnotificationalerttype.md)
- [iOS 通知设置](intune-deviceconfig-iosnotificationsettings.md)
- [iOS 更新配置](intune-deviceconfig-iosupdateconfiguration.md)
- [iOS 更新设备状态](intune-deviceconfig-iosupdatedevicestatus.md)
- [iOS 更新安装状态](intune-deviceconfig-iosupdatesinstallstatus.md)
- [macOS 合规性策略](intune-deviceconfig-macoscompliancepolicy.md)
- [macOS 自定义配置](intune-deviceconfig-macoscustomconfiguration.md)
- [macOS 设备功能配置](intune-deviceconfig-macosdevicefeaturesconfiguration.md)
- [macOS 常规设备配置](intune-deviceconfig-macosgeneraldeviceconfiguration.md)
- [媒体内容分级（澳大利亚）](intune-deviceconfig-mediacontentratingaustralia.md)
- [媒体内容分级（加拿大）](intune-deviceconfig-mediacontentratingcanada.md)
- [媒体内容分级（法国）](intune-deviceconfig-mediacontentratingfrance.md)
- [媒体内容分级（德国）](intune-deviceconfig-mediacontentratinggermany.md)
- [媒体内容分级（爱尔兰）](intune-deviceconfig-mediacontentratingireland.md)
- [媒体内容分级（日本）](intune-deviceconfig-mediacontentratingjapan.md)
- [媒体内容分级（新西兰）](intune-deviceconfig-mediacontentratingnewzealand.md)
- [媒体内容分级（英国）](intune-deviceconfig-mediacontentratingunitedkingdom.md)
- [媒体内容分级（美国）](intune-deviceconfig-mediacontentratingunitedstates.md)
- [Miracast 频道](intune-deviceconfig-miracastchannel.md)
- [OMA 设置](intune-deviceconfig-omasetting.md)
- [OMA 设置 base64](intune-deviceconfig-omasettingbase64.md)
- [OMA 设置布尔值](intune-deviceconfig-omasettingboolean.md)
- [OMA 设置日期/时间](intune-deviceconfig-omasettingdatetime.md)
- [OMA 设置浮点数](intune-deviceconfig-omasettingfloatingpoint.md)
- [OMA 设置整数](intune-deviceconfig-omasettinginteger.md)
- [OMA 设置字符串](intune-deviceconfig-omasettingstring.md)
- [OMA 设置字符串 XML](intune-deviceconfig-omasettingstringxml.md)
- [策略平台类型](intune-deviceconfig-policyplatformtype.md)
- [预发布功能](intune-deviceconfig-prereleasefeatures.md)
- [分级应用类型](intune-deviceconfig-ratingappstype.md)
- [分级澳大利亚电影类型](intune-deviceconfig-ratingaustraliamoviestype.md)
- [分级澳大利亚电视类型](intune-deviceconfig-ratingaustraliatelevisiontype.md)
- [分级加拿大电影类型](intune-deviceconfig-ratingcanadamoviestype.md)
- [分级加拿大电视类型](intune-deviceconfig-ratingcanadatelevisiontype.md)
- [分级法国电影类型](intune-deviceconfig-ratingfrancemoviestype.md)
- [分级法国电视类型](intune-deviceconfig-ratingfrancetelevisiontype.md)
- [分级德国电影类型](intune-deviceconfig-ratinggermanymoviestype.md)
- [分级德国电视类型](intune-deviceconfig-ratinggermanytelevisiontype.md)
- [分级爱尔兰电影类型](intune-deviceconfig-ratingirelandmoviestype.md)
- [分级爱尔兰电视类型](intune-deviceconfig-ratingirelandtelevisiontype.md)
- [分级日本电影类型](intune-deviceconfig-ratingjapanmoviestype.md)
- [分级日本电视类型](intune-deviceconfig-ratingjapantelevisiontype.md)
- [分级新西兰电影类型](intune-deviceconfig-ratingnewzealandmoviestype.md)
- [分级新西兰电视类型](intune-deviceconfig-ratingnewzealandtelevisiontype.md)
- [分级英国电影类型](intune-deviceconfig-ratingunitedkingdommoviestype.md)
- [分级英国电视类型](intune-deviceconfig-ratingunitedkingdomtelevisiontype.md)
- [分级美国电影类型](intune-deviceconfig-ratingunitedstatesmoviestype.md)
- [分级美国电视类型](intune-deviceconfig-ratingunitedstatestelevisiontype.md)
- [所需密码类型](intune-deviceconfig-requiredpasswordtype.md)
- [安全搜索筛选器类型](intune-deviceconfig-safesearchfiltertype.md)
- [设置源](intune-deviceconfig-settingsource.md)
- [设置状态设备摘要](intune-deviceconfig-settingstatedevicesummary.md)
- [共享电脑帐户删除策略类型](intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)
- [共享电脑帐户管理器策略](intune-deviceconfig-sharedpcaccountmanagerpolicy.md)
- [共享电脑允许的帐户类型](intune-deviceconfig-sharedpcallowedaccounttype.md)
- [共享的电脑配置](intune-deviceconfig-sharedpcconfiguration.md)
- [网站安全级别](intune-deviceconfig-sitesecuritylevel.md)
- [软件更新状态摘要](intune-deviceconfig-softwareupdatestatussummary.md)
- [状态管理设置](intune-deviceconfig-statemanagementsetting.md)
- [可见性设置](intune-deviceconfig-visibilitysetting.md)
- [Web 浏览器 cookie 设置](intune-deviceconfig-webbrowsercookiesettings.md)
- [每周计划](intune-deviceconfig-weeklyschedule.md)
- [欢迎屏幕会议信息](intune-deviceconfig-welcomescreenmeetinginformation.md)
- [Windows 10 合规性策略](intune-deviceconfig-windows10compliancepolicy.md)
- [Windows 10 自定义配置](intune-deviceconfig-windows10customconfiguration.md)
- [Windows 10 版本类型](intune-deviceconfig-windows10editiontype.md)
- [Windows 10 终结点保护配置](intune-deviceconfig-windows10endpointprotectionconfiguration.md)
- [Windows 10 企业版新式应用管理配置](intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md)
- [Windows 10 常规配置](intune-deviceconfig-windows10generalconfiguration.md)
- [Windows 10 移动版合规性策略](intune-deviceconfig-windows10mobilecompliancepolicy.md)
- [Windows 10 网络代理服务器](intune-deviceconfig-windows10networkproxyserver.md)
- [Windows 10 安全评估配置](intune-deviceconfig-windows10secureassessmentconfiguration.md)
- [Windows 10 协同版常规配置](intune-deviceconfig-windows10teamgeneralconfiguration.md)
- [Windows 8.1 合规性策略](intune-deviceconfig-windows81compliancepolicy.md)
- [Windows 8.1 常规配置](intune-deviceconfig-windows81generalconfiguration.md)
- [Windows Defender 高级威胁防护配置](intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md)
- [Windows 传递优化模式](intune-deviceconfig-windowsdeliveryoptimizationmode.md)
- [Windows 防火墙网络配置文件](intune-deviceconfig-windowsfirewallnetworkprofile.md)
- [Windows Phone 8.1 合规性策略](intune-deviceconfig-windowsphone81compliancepolicy.md)
- [Windows Phone 8.1 自定义配置](intune-deviceconfig-windowsphone81customconfiguration.md)
- [Windows Phone 8.1 常规配置](intune-deviceconfig-windowsphone81generalconfiguration.md)
- [Windows 聚焦支持设置](intune-deviceconfig-windowsspotlightenablementsettings.md)
- [Windows 开始菜单应用列表可见性类型](intune-deviceconfig-windowsstartmenuapplistvisibilitytype.md)
- [Windows 开始菜单模式类型](intune-deviceconfig-windowsstartmenumodetype.md)
- [Windows 更新使用时段安装](intune-deviceconfig-windowsupdateactivehoursinstall.md)
- [适用于企业的 Windows 更新配置](intune-deviceconfig-windowsupdateforbusinessconfiguration.md)
- [Windows 更新安装计划类型](intune-deviceconfig-windowsupdateinstallscheduletype.md)
- [Windows 更新计划安装](intune-deviceconfig-windowsupdatescheduledinstall.md)
- [Windows 更新类型](intune-deviceconfig-windowsupdatetype.md)
- [Windows 用户帐户控制设置](intune-deviceconfig-windowsuseraccountcontrolsettings.md)






