# Asrock-B460M-ITX-AC-OC-EFI
适用于华擎 B460M-ITX/AC 主板的 OpenCore EFI.

![](https://github.com/Makiny/Asrock-B460M-ITX-AC-OC-EFI/blob/master/images/system%20info.png)
## 硬件配置
| 项目 | 型号 |
| --- | --- |
| 主板 | 华擎B460M-ITX/AC | 
| CPU | Intel i5-10400 |
| 内存 | 镁光DDR4 2666 16G x 1 | 
| 固态 | 西数SN750 500 GB | 
| 集显 | Intel UHD 630 | 
| 独显 | 华擎AMD Radeon RX 6600 XT CLI挑战者| 
| WiFi/蓝牙| 原装BCM94360CS2 | 
| 有线网卡 | 瑞昱RTL8156B USB 2.5G网卡/板载1G网卡 |
| 显示器 | 三星27寸4K(S27A702NWC) |

## 功能正常
- 睡眠/唤醒
- 后置4个USB3/2（其他USB未映射，使用[USBMap](https://github.com/corpnewt/USBMap)进行映射）
- 后置音频接口
- 板载有线网口/瑞昱RTL8156B USB 2.5G网卡
- 6600XT DP 4K@60Hz输出
- iService：Apple ID、App Store、iCloud、iMessage、随航。（没有摄像头，FaceTime未测试）
- Wi-Fi/蓝牙(使用BCM94360CS2)
    - AirPods自动连接、摘下暂停和入耳播放
    - Apple Watch解锁

## 功能故障
Hackintool中的`音频 -> 声音信息 -> 子设备`显示 ？？？（不影响音频功能）

## 使用方式
- 安装完毕后，首先确认iService正常后，再登陆Apple ID
- 在 `config.plist -> PlatForm -> Generic` 中填写你自己的SMBIOS信息([使用GenBIOS生成](https://github.com/corpnewt/GenSMBIOS))
- SMBIOS信息中`ROM`填写`en0`对应网卡的`MAC`地址，若没有en0网卡，参见[修复En0](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#fixing-en0)进行解决
