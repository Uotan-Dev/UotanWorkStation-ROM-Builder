# 通过 Github Action 使用 UotanWorkStation 编译 ROM 和 Recovery

当前支持的ROM（名称_Android版本,顺序为A-Z）：<br/>
1.AlphaDroid_13<br/>
2.AOSPA_13<br/>
3.AOSPA_14<br/>
4.Arrow_13<br/>
5.Cipher_13<br/>
6.crDroid_13<br/>
7.DerpFest_14<br/>
8.DroidX_13<br/>
9.EvolutionX_13<br/>
10.EvolutionX_14<br/>
11.exTHmUI_13<br/>
12.Lineage_13<br/>
13.Lineage_14<br/>
14.Miku_14<br/>
15.PixelExperience_13<br/>
16.PixelExperience_14<br/>
17.RisingTech_13<br/>
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
