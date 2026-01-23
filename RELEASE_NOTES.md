# Release Notes

## January 2026

### Features

- [`6570f4ce`](https://github.com/stitch-05/file-taxes-paraguay/commit/6570f4ce9f11ce247e45d051995d840be1fdda85): Added `.env.example` template file for easier configuration setup
- [`6570f4ce`](https://github.com/stitch-05/file-taxes-paraguay/commit/6570f4ce9f11ce247e45d051995d840be1fdda85): Updated documentation to reflect environment variable changes
- [`7a4829ff`](https://github.com/stitch-05/file-taxes-paraguay/commit/7a4829ff4f222d9ac47298a49ce96df912226049): Added request logging when debug mode is enabled for easier troubleshooting

---

## November 2025

### Features

- [`5776771d`](https://github.com/stitch-05/file-taxes-paraguay/commit/5776771de1b6473250475760ebda6e4a63a745c1): Implemented functionality to automatically download tax statements from the tax authority portal
- [`9950cb2d`](https://github.com/stitch-05/file-taxes-paraguay/commit/9950cb2d2f8447ecdbb7c24b2256f4d58b33ab8c): Rewrote all wget calls for improved reliability and maintainability

### Bug Fixes

- [`0a364814`](https://github.com/stitch-05/file-taxes-paraguay/commit/0a364814a38f68103dbc7098244059f02abc55bd): Fixed error handling in form 211 submission process

---

## September 2025

### Features

- [`ac3f74db`](https://github.com/stitch-05/file-taxes-paraguay/commit/ac3f74db15c7b1180c89b65f96434572bc370bdc): Made environment variables more user-friendly with better naming and documentation
- [`30fafc78`](https://github.com/stitch-05/file-taxes-paraguay/commit/30fafc7877e08c89eebb77e559bf6d17caf49b79): Added command-line arguments for SMTP server configuration
- [`92ce902f`](https://github.com/stitch-05/file-taxes-paraguay/commit/92ce902f43583e72558b4d8b2eeea83d117fe3ca): Implemented database/configuration migration system for version upgrades
- [`92ce902f`](https://github.com/stitch-05/file-taxes-paraguay/commit/92ce902f43583e72558b4d8b2eeea83d117fe3ca): Added automatic environment variable export functionality
- [`45a21f71`](https://github.com/stitch-05/file-taxes-paraguay/commit/45a21f718257ea473e068de4d9d09bcd72ce9725): Added support for script arguments to control execution behavior

### Bug Fixes

- [`a85be76c`](https://github.com/stitch-05/file-taxes-paraguay/commit/a85be76c75b2f45d73b2ff3cd6f5673a79112879): Fixed migration path from version 0.0.1 to 1.0.0

---

## August 2024

### Features

- [`0f1cf8be`](https://github.com/stitch-05/file-taxes-paraguay/commit/0f1cf8bec6de9d4b7d6f83492a38265c74dc54f9): Implemented SMTP email notifications to alert users of tax filing status
- [`0f1cf8be`](https://github.com/stitch-05/file-taxes-paraguay/commit/0f1cf8bec6de9d4b7d6f83492a38265c74dc54f9): Added support for STARTTLS encryption for secure email transmission
- [`08918503`](https://github.com/stitch-05/file-taxes-paraguay/commit/0891850383d2d6461d8ad448fe7f21a5ff3d985c): Added wget as a required dependency in the installation instructions for Mac users
- [`6f901df8`](https://github.com/stitch-05/file-taxes-paraguay/commit/6f901df86018a701a456eb1f543b3ac4bca1e17f): Implemented support for filing tax payer registration forms
- [`1a27370b`](https://github.com/stitch-05/file-taxes-paraguay/commit/1a27370b3c45baa1d96b995cec69680361dcd1e4): Added support for filing percentage of economic activity forms

### Bug Fixes

- [`0474c28b`](https://github.com/stitch-05/file-taxes-paraguay/commit/0474c28b2615be9649f7a6f5c895c07369e8f578): Fixed issues with the percentages form submission

---

## April 2024

### Features

- [`bbadaf36`](https://github.com/stitch-05/file-taxes-paraguay/commit/bbadaf36b67a6d452a214063ad56590f2d65df22): Added more descriptive error messages when requesting forms that haven't been implemented yet

### Bug Fixes

- [`90f79435`](https://github.com/stitch-05/file-taxes-paraguay/commit/90f79435c11c4938effe71fb85f4cf5b75773bb5): Fixed issue where tax filing was requested for new fiscal periods before they officially started

---

## August 2023

### Bug Fixes

- [`a01a9011`](https://github.com/stitch-05/file-taxes-paraguay/commit/a01a90119c063632ee0a96ef9de57866882380e2): Fixed month number parsing to be treated as decimal instead of octal, preventing incorrect date calculations

---

## January 2023

### Features

- [`1177ec54`](https://github.com/stitch-05/file-taxes-paraguay/commit/1177ec5444834406b1a4904279b29dd09a33f011): Added detection and error reporting for CAPTCHA challenges

---

## December 2022

### Features

- [`b2f51458`](https://github.com/stitch-05/file-taxes-paraguay/commit/b2f51458d5c062f9830b06fea56d814e8e45417c): Added notification system to alert users when errors occur during execution

### Bug Fixes

- [`6b7be640`](https://github.com/stitch-05/file-taxes-paraguay/commit/6b7be640860e46d3150d7797a96d369fba602a42): Fixed issue where subscript errors would cause the main script to exit unexpectedly
- [`e8deda56`](https://github.com/stitch-05/file-taxes-paraguay/commit/e8deda5680c227596783be65e601ea01c6124888): Updated to work with changed URLs on the tax authority portal

---
