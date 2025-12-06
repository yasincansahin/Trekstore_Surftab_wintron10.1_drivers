# Driver Verification and Security Guide

## Why Driver Verification Matters

Installing drivers from unofficial sources can pose security risks. This guide helps you verify driver authenticity and safety.

## Before Installing Drivers

### 1. Create a System Restore Point
**Always** create a restore point before installing any drivers:
```
Windows + R → sysdm.cpl → System Protection → Create
```

### 2. Scan for Malware
Use your antivirus software to scan all driver files before installation:
- Windows Defender (built-in)
- Third-party antivirus software
- Online scanners (VirusTotal, etc.)

### 3. Verify File Integrity
If checksums (MD5, SHA256) are provided:

**On Windows PowerShell**:
```powershell
# For MD5
Get-FileHash -Path "driver_file.inf" -Algorithm MD5

# For SHA256
Get-FileHash -Path "driver_file.inf" -Algorithm SHA256
```

Compare the output with the provided checksum.

## Understanding Driver Files

### Safe File Types
These are normal driver file types:
- `.inf` - Driver information file (text file, safe to inspect)
- `.sys` - System driver file
- `.cat` - Catalog file (contains digital signature information)
- `.dll` - Dynamic link library
- `.exe` - Setup executable (verify carefully)
- `.msi` - Windows installer package

### Inspecting .INF Files
You can open `.inf` files with Notepad to see what they do:
```
Right-click on .inf file → Edit
```

Look for:
- Driver name and version
- Hardware IDs (to confirm it's for your device)
- Files being installed

### Digital Signatures
Check if drivers are digitally signed:

1. Right-click on driver file
2. Select "Properties"
3. Go to "Digital Signatures" tab
4. Verify the signer information

**Note**: Older drivers (like these from 2015) may not have valid digital signatures, especially after the signing certificates expired. This is normal for archived drivers.

## Red Flags

### Be Cautious If:
- ❌ Executable files have no description or publisher information
- ❌ Antivirus software flags files
- ❌ Driver is much larger than expected (>50MB for basic drivers)
- ❌ Unknown additional software is bundled
- ❌ Files are obfuscated or encrypted

### Warning Signs During Installation:
- ⚠️ Requests for unnecessary permissions
- ⚠️ Wants to install unrelated software
- ⚠️ Requires disabling antivirus
- ⚠️ Asks for payment
- ⚠️ Redirects to advertisement sites

## Driver Installation Best Practices

### 1. Install One Driver at a Time
Don't install multiple drivers simultaneously. This helps identify which driver causes issues if problems occur.

### 2. Document What You Do
Keep notes of:
- Which drivers you installed
- When you installed them
- Any changes in system behavior
- Restore point names

### 3. Test After Installation
After installing a driver:
1. Restart your system
2. Test the affected hardware
3. Check Device Manager for errors
4. Monitor system stability for a day

### 4. Keep Old Drivers
Before updating, you can export the current driver:
1. Device Manager → Right-click device → Properties
2. Driver tab → Driver Details
3. Note the location of current driver files
4. Copy them to a backup folder

## If Something Goes Wrong

### Safe Mode
If the system becomes unstable:
1. Restart and press F8 repeatedly
2. Select "Safe Mode"
3. Uninstall the problematic driver

### System Restore
If you created a restore point:
```
Windows + R → rstrui.exe → Next
Select restore point → Follow wizard
```

### Last Known Good Configuration
On Windows 8.1:
1. Restart and press F8
2. Select "Last Known Good Configuration"

## Additional Security Tips

### 1. Download from Trusted Sources
- This repository (verified by the community)
- Manufacturer websites (if still available)
- Reputable driver databases

### 2. Keep Windows Updated
Windows Update can provide newer, signed drivers that may work better.

### 3. Use Standard User Account for Testing
If possible, test drivers while logged in as a standard user, not administrator.

### 4. Research Before Installing
- Search for the driver name online
- Look for reviews or reports
- Check forums for others' experiences

## Verifying This Repository

### How to Trust This Repository
1. Check the commit history
2. Look at who contributed
3. Read discussions in issues
4. Verify checksums match
5. Test on non-critical system first

### Community Verification
If you successfully use drivers from this repository:
- Report your experience in issues
- Confirm which files worked
- Share your OS version and setup

## Emergency Contacts

### Microsoft Support
If you experience critical issues:
- Microsoft Support: https://support.microsoft.com
- Windows Community: https://answers.microsoft.com

### Reporting Security Issues
If you find security problems with files in this repository:
1. Do NOT install the file
2. Open a security issue in GitHub
3. Provide details about the concern
4. Include antivirus reports if applicable

---

**Türkçe**

# Sürücü Doğrulama ve Güvenlik Kılavuzu

## Sürücü Doğrulaması Neden Önemlidir

Resmi olmayan kaynaklardan sürücü yüklemek güvenlik riskleri oluşturabilir. Bu kılavuz, sürücü özgünlüğünü ve güvenliğini doğrulamanıza yardımcı olur.

## Sürücüleri Yüklemeden Önce

### 1. Sistem Geri Yükleme Noktası Oluşturun
Herhangi bir sürücü yüklemeden önce **mutlaka** bir geri yükleme noktası oluşturun:
```
Windows + R → sysdm.cpl → Sistem Koruması → Oluştur
```

### 2. Kötü Amaçlı Yazılım Taraması Yapın
Kurulumdan önce tüm sürücü dosyalarını antivirüs yazılımınızla tarayın:
- Windows Defender (yerleşik)
- Üçüncü taraf antivirüs yazılımı
- Çevrimiçi tarayıcılar (VirusTotal, vb.)

### 3. Dosya Bütünlüğünü Doğrulayın
Checksum'lar (MD5, SHA256) sağlanmışsa:

**Windows PowerShell'de**:
```powershell
# MD5 için
Get-FileHash -Path "surucu_dosyasi.inf" -Algorithm MD5

# SHA256 için
Get-FileHash -Path "surucu_dosyasi.inf" -Algorithm SHA256
```

Çıktıyı sağlanan checksum ile karşılaştırın.

## Kırmızı Bayraklar

### Dikkatli Olun:
- ❌ Yürütülebilir dosyaların açıklaması veya yayıncı bilgisi yoksa
- ❌ Antivirüs yazılımı dosyaları işaretlerse
- ❌ Sürücü beklenenden çok daha büyükse (temel sürücüler için >50MB)
- ❌ Bilinmeyen ek yazılım paketlenmişse
- ❌ Dosyalar şifrelenmiş veya gizlenmişse

## Bir Şeyler Ters Giderse

### Güvenli Mod
Sistem kararsız hale gelirse:
1. Yeniden başlatın ve F8'e tekrar tekrar basın
2. "Güvenli Mod"u seçin
3. Sorunlu sürücüyü kaldırın

### Sistem Geri Yükleme
Bir geri yükleme noktası oluşturduysanız:
```
Windows + R → rstrui.exe → İleri
Geri yükleme noktasını seçin → Sihirbazı izleyin
```
