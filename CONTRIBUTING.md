# Contributing to Trekstore Surftab Wintron 10.1 Drivers

Thank you for your interest in contributing to this driver archive!

## How to Contribute

### Adding Drivers
If you have additional drivers for the Trekstore Surftab Wintron 10.1 tablet:

1. **Fork** this repository
2. **Create a new branch** for your contribution
3. **Add the driver files** to the appropriate directory:
   - Touchscreen drivers → `drivers/touchscreen/`
   - Audio drivers → `drivers/audio/`
   - Other drivers → Create a new folder under `drivers/`
4. **Document the drivers**:
   - Add a README.md in the driver folder
   - Include version information
   - Specify what the driver fixes
   - Add installation instructions
   - Include checksums (MD5/SHA256) for verification
5. **Submit a Pull Request**

### Improving Documentation
Documentation improvements are always welcome:
- Fix typos or grammatical errors
- Add translations
- Improve installation instructions
- Add troubleshooting guides
- Update compatibility information

### Adding Translations
If you'd like to add documentation in another language:
1. Create a new README file with the language code (e.g., `README.de.md` for German)
2. Translate the content accurately
3. Update the main README.md to link to the new translation

### Reporting Issues
If you encounter problems:
1. Check if the issue already exists
2. Open a new issue with:
   - Clear description of the problem
   - Your Windows version
   - Steps to reproduce
   - Any error messages

## Guidelines

### File Guidelines
- **Do not commit**: 
  - Executables from unknown sources
  - Files larger than 100MB (use Git LFS or provide download links instead)
  - Copyrighted materials without proper attribution
- **Do commit**:
  - Driver files (.inf, .sys, .cat)
  - Documentation
  - Installation scripts (if safe and well-documented)

### Code of Conduct
- Be respectful and constructive
- Help fellow tablet owners
- Provide accurate information
- Respect copyright and licensing

### Testing
Before contributing drivers:
1. Test them on your own device first
2. Document the testing environment (OS version, etc.)
3. Verify they don't contain malware
4. Include source information if possible

## Questions?
If you have questions about contributing, please open an issue with the "question" label.

---

**Türkçe**

# Trekstore Surftab Wintron 10.1 Sürücülerine Katkıda Bulunma

Bu sürücü arşivine katkıda bulunmak istediğiniz için teşekkür ederiz!

## Nasıl Katkıda Bulunulur

### Sürücü Ekleme
Trekstore Surftab Wintron 10.1 tablet için ek sürücüleriniz varsa:

1. Bu depoyu **fork'layın**
2. Katkınız için **yeni bir dal oluşturun**
3. **Sürücü dosyalarını** uygun dizine ekleyin:
   - Dokunmatik ekran sürücüleri → `drivers/touchscreen/`
   - Ses sürücüleri → `drivers/audio/`
   - Diğer sürücüler → `drivers/` altında yeni bir klasör oluşturun
4. **Sürücüleri belgeleyin**:
   - Sürücü klasörüne bir README.md ekleyin
   - Sürüm bilgisini ekleyin
   - Sürücünün neyi düzelttiğini belirtin
   - Kurulum talimatlarını ekleyin
   - Doğrulama için checksum'ları (MD5/SHA256) ekleyin
5. **Pull Request gönderin**

### Belgelendirmeyi İyileştirme
Belgelendirme iyileştirmeleri her zaman memnuniyetle karşılanır:
- Yazım hatalarını veya gramer hatalarını düzeltin
- Çeviri ekleyin
- Kurulum talimatlarını iyileştirin
- Sorun giderme kılavuzları ekleyin
- Uyumluluk bilgilerini güncelleyin

## Sorular?
Katkıda bulunma hakkında sorularınız varsa, lütfen "soru" etiketi ile bir issue açın.
