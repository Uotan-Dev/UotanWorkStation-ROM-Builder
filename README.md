# 通过 Github Action 使用 UotanWorkStation 编译 ROM 和 Recovery

当前支持的ROM（名称_Android版本,顺序为A-Z）：<br/>
1. AfterLife_13
2. AlphaDroid_13
3. AlphaDroid_14
4. AOSPA_13
5. AOSPA_14
6. Arrow_13
7. Arrow_14
8. AwakenOS_14
9. Cipher_13
10. Cipher_14
11. crDroid_13
12. crDroid_14
13. DroidX_13
14. EvolutionX_13
15. EvolutionX_14
16. exTHmUI_13
17. GrapheneOS_14
18. Lineage_13
19. Lineage_14
20. Miku_14
21. PixelExperience_13
22. PixelExperience_14
23. RisingTech_13
24. RisingTech_14
25. Superior_13
26. Syberia_13
    
*由于ROM编译日志较长，GitHub Action 运行时无法显示全部日志，构建时请耐心等待！错误日志会上传至Artifacts。<br/>

当前支持的Recovery（名称_Android版本,顺序为A-Z）：<br/>
1.OrangeFox_12<br/>
2.TWRP_12<br/>

-----

## 参数说明

| 名称 | 描述 | 示例 |
| ------------ | -------------------- | ------------ |
| `ROM_NAME_ANDROID_VERSION` | 名称_Android版本 | PixelExperience_13（按照支持列表书写）|
| `RECOVERY_NAME` | 名称_Android版本 | TWRP_13（按照支持列表书写）|
| `NAME_VERSION` | 名称_Android版本 | Arrow_13（按照支持列表书写）|
| `ANDROID_OR_RECOVERY` | Android或Recovery | Android |
| `DEVICE_PATH` | 设备文件地址 | oneplus/fajita（品牌名称/设备代号）|
| `DEVICE_TREE_URL_BRANCH` | 设备树链接和分支 | https://github.com/PixelExperience-Devices/device_oneplus_fajita.git -b thirteen |
| `KERNEL_SOURCE_URL_BRANCH` | 内核源码和分支 | https://github.com/PixelExperience-Devices/kernel_oneplus_sdm845.git -b thirteen |
| `KERNEL_SOURCE_PATH` | 内核文件地址 | oneplus/sdm845 |
| `VENDOR_BLOBS_URL_BRANCH` | Vendor Blobs链接和分支 | https://gitlab.pixelexperience.org/android/vendor-blobs/vendor_oneplus_fajita.git -b thirteen |
| `COMMON_TREE_URL_BRANCH` | 通用设备树链接和分支 | https://github.com/PixelExperience-Devices/device_oneplus_sdm845-common -b thirteen |
| `COMMON_BLOBS_URL_BRANCH` | 通用Vendor Blobs链接和分支 | https://gitlab.pixelexperience.org/android/vendor-blobs/vendor_oneplus_sdm845-common.git -b thirteen |
| `COMMON_PATH` | 通用文件地址 | oneplus/sdm845-common |
| `MAKEFILE_NAME_BUILD_TYPE` | Makefile文件名和构建类型 | aosp_fajita-userdebug |
| `BUILD_TARGET` | 构建目标（分区） | recovery |

-----

## 如何使用
#### 前言
该项目使用私有服务器进行构建，Fork后无法直接使用! 如果您想使用我们的服务器进行构建，您可以联系我们:<br/>
QQ: 3089319531<br/>
Telegram: https://t.me/mujianwu<br/>
#### 1、点击 'Actions - ROM Build/Recovery Bulid/Repo Sync'。
![](https://github.com/Uotan-Dev/UotanWorkStation-ROM-Builder/blob/main/PNG/Action.png)
#### 2、点击 'Run workflow' 并按照上文 '参数说明' 填写。
![](https://github.com/Uotan-Dev/UotanWorkStation-ROM-Builder/blob/main/PNG/Workflow.png)
#### 3、填写完成后点击 'Run workflow' 开始运行。

-----

## 高级使用
#### 1、您可以在设备树中添加vendorsetup.sh脚本来拉取设备树以外的依赖文件(如下图)。
![](https://github.com/Uotan-Dev/UotanWorkStation-ROM-Builder/blob/main/PNG/vendorsetup.png)
#### 2、如多次使用相同设备树构建相同ROM您也可以在上述脚本中添加判断来确定是否需要重新拉取依赖文件，或对依赖文件进行更新。

-----

## 编译结果
- 构建成功可以前往Release下载。
- 构建失败可以前往Artifacts获取错误日志。
