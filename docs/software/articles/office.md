# office 365

## 按需求安装

office365 通常会安装 Word/Excel/PPT/Publisher/OneDrive/Outlook/Access，但实际使用以 Word/Excel/PPT 为主，想删除多余的却没有入口。

这里将使用 ODT（Office Deployment Tool）Office 部署管理工具，完成此次任务。

下载 [ODT](https://www.microsoft.com/en-us/download/confirmation.aspx?id=49117)

解压：建议新建一个文件夹，运行下载文件，点击同意，选择刚刚建的文件夹

编辑配置文件：ODT 包含 两类文件：setup.exe 和 configuration.xml。

修改 `configuration-Office365-x64.xml`

```cmd
<Configuration>

<Add OfficeClientEdition="64" Channel="Current">
<Product ID="O365ProPlusRetail">
<Language ID="zh-cn" />
<ExcludeApp ID = "Publisher"/>
<ExcludeApp ID = "Groove"/>
<ExcludeApp ID = "OneNote"/>
<ExcludeApp ID = "Bing"/>
<ExcludeApp ID = "lync"/>
<ExcludeApp ID = "Access"/>
<ExcludeApp ID = "Outlook"/>
<ExcludeApp ID = "Teams"/>
<ExcludeApp ID = "Skype"/>
</Product>

</Add>

<Updates Enabled="TRUE" Channel="Current" />

  <!--  <Display Level="None" AcceptEULA="TRUE" />  -->

  <!--  <Property Name="AUTOACTIVATE" Value="1" />  -->

</Configuration>
```

简单解释

`64`：安装 64 位版本

`O365ProPlusRetail`：下载并安装 Microsoft 365 企业应用版

`zh-cn`：下载并安装中文

`ExcludeApp ID = "Publisher"`：定义不应安装哪些 Microsoft 365 应用版产品。 以此类推。

`Updates Enabled="TRUE"`：检查更新

执行命令

cmd：`setup.exe /configure configuration-Office365-x64.xml`

PowerShell： `./setup.exe /configure configuration-Office365-x64.xml`

## 更多阅读

- [Office 部署工具的配置选项](https://learn.microsoft.com/zh-cn/deployoffice/office-deployment-tool-configuration-options)

- [Microsoft 365 应用版的更新历史记录](https://learn.microsoft.com/zh-cn/officeupdates/update-history-microsoft365-apps-by-date)

- [Office365 卸载捆绑软件Publisher/OneDrive/Outlook/Access](https://zhuanlan.zhihu.com/p/474539463)
