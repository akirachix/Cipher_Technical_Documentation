# Frontend Mobile

## 1. Overview

The FikaMarket mobile application is a **Flutter-based smartphone application for buyers**.

Buyers use the application to:

* Register and log in
* Browse available produce
* Add produce to their cart
* Place orders
* Manage their profile
* Request help

Farmers do not use the mobile application. Farmers with feature phones interact with FikaMarket through **USSD**.

---

## 2. Tech Stack

| Component   | Technology       |
| ----------- | ---------------- |
| Framework   | Flutter          |
| Language    | Dart             |
| Platform    | Android / iOS    |
| Backend API | FastAPI REST API |
| Database    | PostgreSQL       |

---

## 3. Project Structure

```text
fikamarket/
├── android/
├── ios/
├── assets/
└── lib/
    ├── models/
    │   ├── cart_model.dart
    │   ├── product_item.dart
    │   └── user_profile.dart
    │
    ├── screens/
    │   ├── home_screen.dart
    │   ├── login_screen.dart
    │   ├── signup_screen.dart
    │   ├── market_place.dart
    │   └── buyer_profile_screen.dart
    │
    └── services/
```

---

## 4. Architecture Layers

| Layer        | Purpose                                                                   |
| ------------ | ------------------------------------------------------------------------- |
| **Models**   | Represent application data such as products, users and carts              |
| **Screens**  | Provide the buyer interface                                               |
| **Services** | Communicate with the FikaMarket backend and handle application operations |

```text
Buyer
 ↓
Flutter Mobile App
 ↓
Services
 ↓
FikaMarket API
 ↓
Database
```

---

## 5. Core Components

* **Routing** — handled through `main_navigation_screen.dart`
* **Authentication** — handled through `login_screen.dart` and `signup_screen.dart`
* **Marketplace** — buyers browse produce through `market_place.dart`
* **Cart** — managed through `cart_model.dart`
* **API Service** — communicates with the FikaMarket backend
* **Profile** — manages buyer profile information

---

## 6. Security Measures

The mobile application communicates with the FikaMarket API and does not access the database directly.

Security includes:

* User authentication
* Input validation
* Secure API communication
* Controlled access to user information

The backend provides additional authentication, authorization, and security controls.

See the [Security Architecture](https://drive.google.com/file/d/1qeOpj85cGDaxafPCQVPepJ8V51C2uLMO/view?usp=sharing) documentation for more information.

---

## 7. Installation

### Prerequisites

* Flutter SDK
* Dart
* Git
* Android Studio or Android emulator


### Setup

```bash
git clone <repository-url>
cd fikamarket
flutter pub get
flutter run
```

Check the Flutter environment with:

```bash
flutter doctor
```

---

## 8. Troubleshooting

| Problem                   | Solution                                     |
| ------------------------- | -------------------------------------------- |
| Dependencies fail         | Run `flutter pub get`                        |
| Flutter environment error | Run `flutter doctor`                         |
| API connection fails      | Check the backend URL and availability       |
| Emulator does not start   | Check emulator configuration                 |
| Build errors              | Check Flutter/Dart versions and dependencies |

### Farmer Connectivity

Farmers using **feature phones** do not depend on the Flutter application. Their interaction with FikaMarket is through the **USSD service**, which is designed for environments where smartphone access or reliable internet connectivity may not be available.

```text
Farmer
  ↓
Feature Phone
  ↓
USSD
  ↓
Africa's Talking
  ↓
FikaMarket API
```


