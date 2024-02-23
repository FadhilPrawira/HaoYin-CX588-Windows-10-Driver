# Windows 10 driver for portable Bluetooth and USB thermal printer HaoYin CX588
> Disclaimer: Use at your own risk

This is a Windows 10 driver for portable Bluetooth and USB thermal printer HaoYin CX588. It was obtained from Windows PowerShell command `Export-WindowsDriver -Online -Destination C:\drivers`. 
<table>
  <thead>
    <tr>
      <th>Device name</th>
      <th>Another name</th>
      <th>Bluetooth name</th>
      <th>Manufacturer</th>
      <th>Hardware ids</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">CX588 Bluetooth Thermal Receipt Printer – (2 Inch)</td>
      <td>EPPOS EPX588</td>
      <td rowspan="2">RPP02N</td>
      <td rowspan="2">
        <a href="https://www.f2ctechnology.com/product/cx588-bluetooth-printer/">F2C Technology</a>
      </td>
      <td>USB\VID_09C5&PID_588E&REV_0100</td>
    </tr>
    <td>Blueprint ECO58</td>
    <td>USB\VID_09C5&PID_588E</td>
    <tr></tr>
  </tbody>
</table>

# How to backup driver
1. Turn on your printer. Connect it with the USB cable to your computer/laptop.
2. Install the driver in Windows 7, 8, or 10. I use it on Windows 10.
3. Open your PowerShell as administrator 
```powershell
Export-WindowsDriver -Online -Destination C:\drivers
```

If your folder name have spaces, you can use the quotation mark ("). Example:
```powershell
Export-WindowsDriver -Online -Destination "C:\exported drivers"
```
4. Your drivers will appear in the folder you selected. Find the subfolder that starts with ***pos58.inf***
References:
- [Export-WindowsDriver (DISM) | Microsoft Learn](https://learn.microsoft.com/en-us/powershell/module/dism/export-windowsdriver?view=windowsserver2022-ps)

# How to restore/install driver in Windows 11
1. Download from here. [pos58.inf_amd64_d0244a221378af46.zip](https://github.com/FadhilPrawira/HaoYin-CX588-Windows-10-Driver/releases/download/11.2.0.0/pos58.inf_amd64_d0244a221378af46.zip)
2. Extract the file **pos58.inf_amd64_d0244a221378af46.zip**.

![Extract the file pos58.inf_amd64_d0244a221378af46.zip.](/image/1.png)
3. Turn on your printer. Connect it with the USB cable to your computer/laptop.
4. Open your **Settings** (shortcut ⊞+I). 
5. Select **Bluetooth & devices**. Select **Printers & scanners**.

![Select Bluetooth & devices.](/image/2.png)

![Select Printers & scanners.](/image/3.png)

6. On the right side, you will find button named **Add device**, press it. Wait for a while (It might show you the printer named RPP02N, we will not use it by bluetooth). It will show **The printer that I want isn't listed - Add manually**, press it.

![On the right side, you will find button named Add device, press it.](/image/4.png)

![Wait for a while (It might show you the printer named RPP02N, we will not use it by bluetooth). It will show The printer that I want isn't listed - Add manually, press it.](/image/5.png)

7. Click **Add a local printer or network printer with manual settings**.

![Click Add a local printer or network printer with manual settings.](/image/6.png)

8. Click the option **Use an existing port**. From the dropdown box, select **USB001 (HaoYin CX588)**. It may be has different name in your computer/laptop, just select the one that seems like printer.

![Click the option Use an existing port. From the dropdown box, select USB001 (HaoYin CX588). It may be has different name in your computer/laptop, just select the one that seems like printer.](/image/7.png)

9. Click the **Have Disk** and browse the folder **pos58.inf_amd64_d0244a221378af46**. Select file pos58.inf and press Open.

![Click the Have Disk](/image/8.png)

![Click Browse to browse the driver folder](/image/9.png)

![Find the folder pos58.inf_amd64_d0244a221378af46. Select file pos58.inf and press Open.](/image/10.png)

![Make sure it has the right path to folder pos58.inf_amd64_d0244a221378af46. Click OK.](/image/11.png)

![Make sure the driver's name is POS-58 11.2.0.0. Click next.](/image/12.png)

10. When asked about **Type a printer name**, you can use the default one or change it. We will not change it here.

![When asked about Type a printer name, you can use the default one or change it. We will not change it here.](/image/13.png)

11. In **Printer Sharing**, choose **Do not share this printer**. If you want to share it, choose the bottom option.

![In Printer Sharing, choose Do not share this printer. If you want to share it, choose the bottom option.](/image/14.png)

12. Here you go! We already finished set the HaoYin CX588 printer. You can print a test page, it will be consuming approximately 22.5 cm (For banana fans, approximately 1.107 bananas. For inch fans, approximately 8.858 inch).

![You can print a test page here.](/image/15.png)

![The test page result.](/image/16.png)

Tested in:
- Windows 11 Version 23H2 (OS Build 22631.3155)