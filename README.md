<div align="center">

# E-POS Fiscal Bridge

**Локальный мост между клиентским ПО и фискальным модулем**

[![Download latest](https://img.shields.io/github/v/release/E-POS-Systems/fiscal-bridge?style=for-the-badge&logo=windows&logoColor=white&label=Скачать&color=388392)](https://github.com/E-POS-Systems/fiscal-bridge/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows_10+-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![.NET 8](https://img.shields.io/badge/.NET-8.0_LTS-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)

[Веб-сайт](https://epos.uz) · [Документация](https://docs.epos.uz) · [Скачать](https://github.com/E-POS-Systems/fiscal-bridge/releases/latest)

</div>

---

## О продукте

E-POS Fiscal Bridge — локальный Windows-сервис, прослойка между клиентским ПО (CRM, ERP, кассой) и фискальным модулем. Унифицирует доступ к фискальной функциональности через REST API на `127.0.0.1`, чтобы интеграторам не приходилось работать напрямую с разными драйверами.

```
Client → Fiscal Bridge API (:7200) → Fiscal Module (HTTP localhost)
              ↓
       React GUI (:7100)
              ↓
          Tray app
```

## Установка

1. Скачать последний [`FiscalBridge-win-Setup.exe`](https://github.com/E-POS-Systems/fiscal-bridge/releases/latest)
2. Right-click → **Запуск от имени администратора** (нужно для регистрации Windows Service)
3. После установки Windows Service `FiscalBridge` стартует автоматически
4. Проверить работу: `curl http://127.0.0.1:7200/health`

Бинарники: `%LocalAppData%\FiscalBridge\` Данные и логи: `C:\Users\Public\uz.epos.fiscalbridge\`

## Поддержка

| | |
|---|---|
| 📞 | [+998 71 200 01 73](tel:+998712000173) |
| ✉️ | [support@epos.uz](mailto:support@epos.uz) |
| 🌐 | [epos.uz](https://epos.uz) |
| 🕘 | Пн–Вс, 9:00 — 00:00 |

## Лицензия

Proprietary © 2026 E-POS Systems. Все права защищены.

Исходный код является собственностью E-POS Systems и распространяется только в рамках лицензионных соглашений. Для запросов о доступе к коду — `support@epos.uz`.
