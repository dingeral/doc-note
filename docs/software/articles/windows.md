# 使用 Windows

> 强烈建议通过商业途径。

## 一种使用 HWID 激活的新方法

2015 年微软推出 Windows 10 时，允许 Windows 7 和 Windows 8.1 用户免费升级到 Windows 10，不需要额外购买许可证、不需要任何付费。这种情况也延续到了 Windows 11。

虽然已经过去了 8 年，但是从 Windows 7/8.1 免费升级 Windows 10/11 并激活的渠道一直存在。所以有人利用这个办法开发 HWID (Hardware Identification，硬件标识符) 相关的激活工具，将硬件 ID 发送给微软服务器，从微软服务器获得合法的数字权利许可证进行激活。

获得许可证后，重装系统仍然可以自动激活，这个许可证还可以转移到其他 PC 用于激活。

### 方法 1 - PowerShell（推荐）

在 Windows 8.1/10/11 上，右键单击 Windows 开始菜单，然后选择运行 PowerShell（不是 CMD）。

复制粘贴以下代码并按 Enter

`irm https://massgrave.dev/get | iex`

由于开发者服务器位于国外按回车执行命令时需要获取数据流，数据流获取速度较慢、请耐心等待自动弹窗。

弹窗出现后，使用 HWID 永久激活 Windows 系统请按 1；使用 Ohook 永久激活 Office 请按 2；使用 KMS38 激活 Windows 系统至 2038 年请按 3；使用在线 KMS 激活 Windows/Office 请按 4（在线激活 180 天有效期到期后重新激活）。

### 方法 2

下载 zip 文件 (https://t.me/gaomutongxue/5051) 并解压

在解压后的文件夹中，进入 MAS/All-In-One-Version 文件夹，运行 MAS_AIO.cmd

脚本窗口会给出多个选项，使用 HWID 永久激活 Windows 系统请按 1；使用 Ohook 永久激活 Office 请按 2；使用 KMS38 激活 Windows 系统至 2038 年请按 3；使用在线 KMS 激活 Windows/Office 请按 4（在线激活 180 天有效期到期后重新激活）。

## HEU_KMS_Activator

更适合国人体质

https://github.com/zbezj/HEU_KMS_Activator

## 来源

- https://massgrave.dev/hwid.html
- https://github.com/massgravel/Microsoft-Activation-Scripts