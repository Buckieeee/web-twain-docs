---
layout: default-layout
noTitleIndex: true
needAutoGenerateSidebar: true
title: General troubleshooting steps
keywords: Dynamic Web TWAIN, Error Troubleshooting, general steps, verbose
breadcrumbText: General troubleshooting steps
description: General troubleshooting steps
permalink: /faq/general-troubleshooting-steps.html
---

# Error Troubleshooting

## General troubleshooting steps

- Try our online demo and see if you can reproduce the issue.
- Check the console or network log and report any errors.
- Enable and collect verbose logs (detailed below)

### How to enable and collect verbose log

1. Remove any old log files from
  - Windows `C:\Windows\SysWOW64\Dynamsoft\DynamsoftServicex64_17\log` or `C:\Users\{UserName}\AppData\Roaming\Dynamsoft\DynamsoftService\log`
  - macOS, `Go > Applications > Dynamsoft > DynamsoftServicex64_17 > {installed version No.} > log`
  - Linux, `/opt/dynamsoft/DynamsoftService/log`

2. Set the log level
  - For only one client machine, add the line `LogLevel=14` to `DSConfiguration.ini` on that specific machine.
  - For all client machines, set [ `LogLevel` ]({{site.info}}api/WebTwain_Util.html#loglevel) to 1 in your code. This property should be set as soon as the `WebTwain` instance is created. For example, in the event `Dynamsoft_OnReady`
    ```javascript
    function Dynamsoft_OnReady() {
      DWObject = Dynamsoft.DWT.GetWebTwain("dwtcontrolContainer");
      DWObject.LogLevel = 1;
    }
    ```

3. Reproduce the issue

4. Zip the log files and share with [Dynamsoft Support Team]({{site.about}}getsupport.html) via email.
  - On Windows, the log files are in `C:\Windows\SysWOW64\Dynamsoft\DynamsoftServicex64_17\log` or `C:\Users\{UserName}\AppData\Roaming\Dynamsoft\DynamsoftService\log`
  - On macOS, the log files are in `Go > Applications > Dynamsoft > DynamsoftServicex64_17 > {installed version No.} > log`
  - On Linux, the log files are in `/opt/dynamsoft/DynamsoftServicex64_17/log`
