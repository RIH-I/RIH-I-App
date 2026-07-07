# 🌍 RIH-I — Relief Information Hub International
### نظام إدارة المساعدات الإنسانية | Humanitarian Aid Management System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Flutter](https://img.shields.io/badge/Flutter-3.x-blue.svg)](https://flutter.dev)
[![Supabase](https://img.shields.io/badge/Supabase-Backend-green.svg)](https://supabase.com)
[![Sphere Standards](https://img.shields.io/badge/Sphere-Standards%20Compliant-teal.svg)](https://sphere-standards.org)
[![GDPR](https://img.shields.io/badge/GDPR-Compliant-blue.svg)](https://gdpr.eu)

---

## 📌 About the Project

**RIH-I** is a humanitarian aid management mobile application built to streamline relief operations in conflict zones and disaster-affected areas. The system digitizes the entire aid delivery process — from family registration to distribution verification — ensuring transparency, accountability, and data protection.

> Developed in response to the humanitarian crisis in **Gaza, Palestine** 🇵🇸

---

## 🎯 Key Features

| Feature | Description |
|---------|-------------|
| 👨‍👩‍👧‍👦 Family Registration | Field registration with GPS coordinates and priority scoring |
| 📊 Smart Prioritization | AI-based algorithm to rank families by need level |
| 📦 Aid Distribution Tracking | QR Code + Blockchain Hash verification system |
| 📴 Offline Mode | SQLite local storage with automatic cloud sync |
| 🔔 Real-time Notifications | Instant updates on request status changes |
| 📋 5Ws International Reports | WHO, WHAT, WHERE, WHEN, WHY reporting format |
| 🔐 Data Security | SSL + MD5 encryption + Row Level Security |
| 🌐 Multilingual | Full Arabic and English support |

---

## 👥 User Roles

```
┌─────────────────────────────────────────────────┐
│  ADMIN          → Full system control & reports  │
│  FIELD WORKER   → Family registration & tasks    │
│  BENEFICIARY    → Track aid & view QR code       │
│  PARTNER/DONOR  → Project monitoring dashboard   │
└─────────────────────────────────────────────────┘
```

---

## 🏗️ Technology Stack

- **Frontend:** Flutter (Dart)
- **Backend:** Supabase (PostgreSQL)
- **Local Storage:** SQLite via `sqflite`
- **Authentication:** Supabase Auth + Custom family login
- **Security:** SSL enforcement, Row Level Security (RLS), MD5 hashing
- **Maps/GPS:** Geolocator package
- **QR System:** `qr_flutter` with Blockchain Hash verification

---

## 📱 Screenshots

> Coming soon — field testing in progress

---

## 🛡️ Standards & Compliance

- ✅ **Sphere Standards** — Humanitarian aid delivery principles
- ✅ **GDPR Compliant** — Full data protection and privacy rights
- ✅ **ICRC Data Protection** — Humanitarian data protection principles
- ✅ **5Ws Reporting** — International humanitarian reporting format
- ✅ **SSL Enforced** — All data encrypted in transit and at rest

---

## 🗄️ Database Schema (Key Tables)

```
families          → Core beneficiary registry
Members           → Individual family member records  
Requests          → Aid request management
Receipts          → Distribution verification & QR codes
Volunteers        → Field worker management
PriorityScores    → Smart prioritization scores
Notifications     → Real-time alert system
Impact_Reports    → Humanitarian impact tracking
Locations         → Distribution point management
```

---

## ⚙️ Setup & Installation

### Prerequisites
- Flutter SDK 3.x
- Dart SDK
- Supabase account

### Installation

```bash
# Clone the repository
git clone https://github.com/RIH-I/RIH-I.git

# Navigate to project
cd RIH-I

# Install dependencies
flutter pub get

# Run the app
flutter run
```

### Environment Configuration
Update `main.dart` with your Supabase credentials:
```dart
await Supabase.initialize(
  url: 'YOUR_SUPABASE_URL',
  anonKey: 'YOUR_SUPABASE_ANON_KEY',
);
```

---

## 📦 Dependencies

```yaml
supabase_flutter: ^2.0.0    # Backend & Auth
sqflite: ^2.3.0             # Local offline storage
connectivity_plus: ^6.0.0   # Network monitoring
qr_flutter: ^4.1.0          # QR code generation
geolocator: ^13.0.0         # GPS location capture
crypto: ^3.0.3              # Password encryption
shared_preferences: ^2.2.0  # Local session storage
permission_handler: ^11.3.1 # Device permissions
```

---

## 🔒 Security Features

- **SSL Enforcement** — Rejects all non-encrypted connections
- **Row Level Security** — Users only access authorized data
- **MD5 Password Hashing** — Passwords never stored in plain text
- **QR + Blockchain Hash** — Tamper-proof distribution receipts
- **Audit Logs** — Complete operation trail for accountability
- **Offline Encryption** — Local data stored securely

---

## 🌍 Deployment Regions

- 🇵🇸 Palestine (Primary)
- Designed for international humanitarian operations globally

---

## 📄 Documentation

- [Privacy Policy (Arabic)](privacy_policy_ar.md)
- [Privacy Policy (English)](privacy_policy_en.md)
- [Sphere Standards Compliance](sphere_standards_screen.dart)

---

## 📬 Contact

- **Email:** rihi.info@gmail.com
- **Project:** Relief Information Hub International — RIH-I
- **Status:** Beta — Field Testing Phase

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

*Built with ❤️ for humanity — Gaza, Palestine 🇵🇸*
