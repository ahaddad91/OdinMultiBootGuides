🔙 [Windows Dual Boot Instructions](https://github.com/ahaddad91/OdinMultiBootGuides/blob/main/pages/odin_dualboot_windows_guide.md)

[Mandatory Tweaks](https://docs.google.com/spreadsheets/d/1FWoHbTymzHX0w9wPf5sNIoR_hEGEV3YHg1achKPnl-0/edit?pli=1&gid=1402553146#gid=1402553146)

Download everything in the essentials sheet in the link above. I am working to condense the process here.

Other tweaks

You can use winutil to debloat windows after installation, but I recommend using only the "tweaks" tab, don't use it to install softwares or to mess with windows update: https://github.com/ChrisTitusTech/winutil

Do not install Borderless Gaming as it seems to corrupt Windows installation.

Do not try to remove Test Mode watermark using "Bcdedit.exe -set TESTSIGNING OFF" it will cause boot error

Do not try to remove Test Mode watermark with 3rd party tools, some are flagged with virus, others cause boot error / system corruption

Activate .NET 2.0 and 3.5 from control panel: https://www.howtogeek.com/880208/how-to-enable-net-framework-2-0-and-3-5-in-windows-11/

Install Visual C++ Redistributable:(ARM64, X86 and X64): https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170

Install OpenCL™ and OpenGL® Compatibility Pack

Install DirectX Runtime: https://www.microsoft.com/en-us/download/details.aspx?id=35

You can use dControl to disable Windows Defender to squeeze a little bit more of performance:

https://www.sordum.org/9480/defender-control-v2-1/

DO AT YOUR OWN RISK!!!! You have to disable Windows Defender real time protection before downloading dControl

And you are good to go.
