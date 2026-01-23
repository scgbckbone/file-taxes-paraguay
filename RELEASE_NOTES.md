# Release Notes

## 6570f4ce9f11ce247e45d051995d840be1fdda85

### Features

- Added `.env.example` template file for easier configuration setup
- Updated documentation to reflect environment variable changes

---

## 5776771de1b6473250475760ebda6e4a63a745c1

### Features

- **Download Tax Statements**: Implemented functionality to automatically download tax statements from the tax authority portal

---

## 9950cb2d2f8447ecdbb7c24b2256f4d58b33ab8c

### Features

- **Refactored HTTP Requests**: Rewrote all wget calls for improved reliability and maintainability

---

## 7a4829ff4f222d9ac47298a49ce96df912226049

### Features

- **Enhanced Debugging**: Added request logging when debug mode is enabled for easier troubleshooting

---

## 0a364814a38f68103dbc7098244059f02abc55bd

### Bug Fixes

- Fixed error handling in form 211 submission process

---

## ac3f74db15c7b1180c89b65f96434572bc370bdc

### Features

- **Improved Configuration**: Made environment variables more user-friendly with better naming and documentation

---

## 30fafc7877e08c89eebb77e559bf6d17caf49b79

### Features

- **SMTP Configuration**: Added command-line arguments for SMTP server configuration

---

## 0f1cf8bec6de9d4b7d6f83492a38265c74dc54f9

### Features

- **Email Notifications**: Implemented SMTP email notifications to alert users of tax filing status
- Added support for STARTTLS encryption for secure email transmission

---

## 92ce902f43583e72558b4d8b2eeea83d117fe3ca

### Features

- **Migration System**: Implemented database/configuration migration system for version upgrades
- Added automatic environment variable export functionality

---

## a85be76c75b2f45d73b2ff3cd6f5673a79112879

### Bug Fixes

- Fixed migration path from version 0.0.1 to 1.0.0

---

## 45a21f718257ea473e068de4d9d09bcd72ce9725

### Features

- **Command-Line Arguments**: Added support for script arguments to control execution behavior

---

## 0891850383d2d6461d8ad448fe7f21a5ff3d985c

### Features

- **macOS Support**: Added wget as a required dependency in the installation instructions for Mac users

---

## 6f901df86018a701a456eb1f543b3ac4bca1e17f

### Features

- **Tax Payer Registration Form**: Implemented support for filing tax payer registration forms

---

## 1a27370b3c45baa1d96b995cec69680361dcd1e4

### Features

- **Economic Activity Percentage Form**: Added support for filing percentage of economic activity forms

---

## 0474c28b2615be9649f7a6f5c895c07369e8f578

### Bug Fixes

- Fixed issues with the percentages form submission

---

## bbadaf36b67a6d452a214063ad56590f2d65df22

### Features

- **Better Error Messages**: Added more descriptive error messages when requesting forms that haven't been implemented yet

---

## 90f79435c11c4938effe71fb85f4cf5b75773bb5

### Bug Fixes

- Fixed issue where tax filing was requested for new fiscal periods before they officially started

---

## a01a90119c063632ee0a96ef9de57866882380e2

### Bug Fixes

- Fixed month number parsing to be treated as decimal instead of octal, preventing incorrect date calculations

---

## 1177ec5444834406b1a4904279b29dd09a33f011

### Features

- **CAPTCHA Error Handling**: Added detection and error reporting for CAPTCHA challenges

---

## 6b7be640860e46d3150d7797a96d369fba602a42

### Bug Fixes

- Fixed issue where subscript errors would cause the main script to exit unexpectedly

---

## e8deda5680c227596783be65e601ea01c6124888

### Bug Fixes

- Updated to work with changed URLs on the tax authority portal

---

## b2f51458d5c062f9830b06fea56d814e8e45417c

### Features

- **Error Notifications**: Added notification system to alert users when errors occur during execution

---
