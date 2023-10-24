# 通过 Github Action 使用 UotanWorkStation 编译 ROM 和 Recovery

当前支持的ROM（名称_Android版本,顺序为A-Z）：<br/>
1.AlphaDroid_13<br/>
2.AOSPA_13<br/>
3.Arrow_13<br/>
4.crDroid_13<br/>
5.DroidX_13<br/>
6.EvolutionX_13<br/>
7.EvolutionX_14<br/>
8.exTHmUI_13<br/>
9.Lineage_13<br/>
10.PixelExperience_13<br/>
11.RisingTech_13<br/>

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
| `ROM_OR_RECOVERY` | Android或Recovery | Android |
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
![](https://github.com/uotandev/UotanWorkStation-ROM-Builder/blob/main/PNG/Action.png)
#### 2、点击 'Run workflow' 并按照上文 '参数说明' 填写。
![](https://github.com/uotandev/UotanWorkStation-ROM-Builder/blob/main/PNG/Workflow.png)
#### 3、填写完成后点击 'Run workflow' 开始运行。

-----

## 编译结果
- 构建成功可以前往Release下载。
- 构建失败可以前往Artifacts获取错误日志。
