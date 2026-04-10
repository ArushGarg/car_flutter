# 🚗 SparkleWash — Premium Car Care, On Demand

A feature-rich mobile application built with **Flutter** and **Firebase** that lets users book professional car wash and detailing services at their doorstep.

---

## 📱 Screenshots

<table>
  <tr>
    <td align="center"><b>Splash</b></td>
    <td align="center"><b>Login</b></td>
    <td align="center"><b>Home</b></td>
    <td align="center"><b>Booking</b></td>
    <td align="center"><b>Confirmation</b></td>
  </tr>
  <tr>
    <td><img src="![WhatsApp Image 2026-03-17 at 11 36 22 PM](https://github.com/user-attachments/assets/83176eae-74e2-4572-affc-0d975c94e079)
" width="160"/></td>
    <td><img src="![WhatsApp Image 2026-03-17 at 11 36 22 PM (1)](https://github.com/user-attachments/assets/c1a24588-dee6-485b-bca4-3e50a97933e6)
" width="160"/></td>
    <td><img src="![WhatsApp Image 2026-03-17 at 11 36 23 PM (1)](https://github.com/user-attachments/assets/d3fff7ef-295e-4f23-b74f-f187bdf40d03)
" width="160"/></td>
    <td><img src="![WhatsApp Image 2026-03-17 at 11 36 23 PM (2)](https://github.com/user-attachments/assets/0678e087-9c9f-4aaf-a9db-29ac5dd82f29)
" width="160"/></td>
    <td><img src="![WhatsApp Image 2026-03-17 at 11 36 23 PM](https://github.com/user-attachments/assets/1cb38761-586f-40cb-b968-3317e33876e7)
" width="160"/></td>
  </tr>
</table>

> **Note:** Place your screenshots in a `screenshots/` folder at the root of the project.

---

## ✨ Features

- **Splash Screen** — Branded loading screen with animated entry
- **Authentication** — Email/password login and Google Sign-In via Firebase Auth
- **Home Dashboard** — Personalized greeting, upcoming appointment card, and service catalogue
- **Service Catalogue** — Browse Basic Wash, Full Detail, Interior Clean, and Premium Pack
- **Appointment Booking** — Select date and time slot, then confirm your booking
- **Booking Confirmation** — Full receipt-style summary with service, date, time, and total
- **Bookings History** — View all past and upcoming appointments
- **Profile Management** — User profile page

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter (Dart) |
| Authentication | Firebase Authentication (Email + Google) |
| Database | Cloud Firestore |
| Backend Logic | Firebase Cloud Functions *(optional)* |
| State Management | Provider / Riverpod *(as applicable)* |
| UI | Custom dark-themed Material Design |

---

## 📁 Project Structure

```
sparklewash/
├── lib/
│   ├── main.dart
│   ├── firebase_options.dart
│   ├── models/
│   │   ├── booking.dart
│   │   └── service.dart
│   ├── screens/
│   │   ├── splash_screen.dart
│   │   ├── login_screen.dart
│   │   ├── home_screen.dart
│   │   ├── booking_screen.dart
│   │   └── confirmation_screen.dart
│   ├── services/
│   │   ├── auth_service.dart
│   │   └── firestore_service.dart
│   └── widgets/
│       ├── service_card.dart
│       └── appointment_card.dart
├── assets/
│   └── images/
├── screenshots/
├── pubspec.yaml
├── google-services.json        # Android (not committed — add to .gitignore)
└── GoogleService-Info.plist    # iOS (not committed — add to .gitignore)
```

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK `>=3.0.0`
- Dart SDK `>=3.0.0`
- A Firebase project (free Spark plan works)
- Android Studio / VS Code with Flutter plugin

### 1. Clone the repository

```bash
git clone https://github.com/your-username/sparklewash.git
cd sparklewash
```

### 2. Set up Firebase

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. Add an **Android** and/or **iOS** app.
3. Download `google-services.json` (Android) and `GoogleService-Info.plist` (iOS) and place them in the correct directories.
4. Enable **Authentication** (Email/Password + Google Sign-In).
5. Create a **Firestore** database in test mode.

### 3. Configure FlutterFire

```bash
dart pub global activate flutterfire_cli
flutterfire configure
```

### 4. Install dependencies

```bash
flutter pub get
```

### 5. Run the app

```bash
flutter run
```

---

## 🔥 Firebase Firestore Structure

```
users/
  {userId}/
    name: "Arush Garg"
    email: "arush@example.com"
    createdAt: Timestamp

bookings/
  {bookingId}/
    userId: string
    service: "Full Detail"
    date: "2026-03-18"
    time: "3:00 PM"
    total: 599
    status: "confirmed"
    createdAt: Timestamp
```

---

## 💳 Services & Pricing

| Service | Price | Duration |
|---|---|---|
| Basic Wash | ₹199 | ~30 min |
| Full Detail | ₹599 | ~90 min |
| Interior Clean | ₹399 | ~60 min |
| Premium Pack | ₹999 | ~120 min |

---

## 🔐 Environment & Security

- Never commit `google-services.json` or `GoogleService-Info.plist` to version control.
- Add them to `.gitignore`:

```
# Firebase config
android/app/google-services.json
ios/Runner/GoogleService-Info.plist
```

- Use Firebase Security Rules to restrict Firestore access to authenticated users only.

---

## 🗺️ Roadmap

- [ ] Push notifications for appointment reminders
- [ ] In-app payment integration (Razorpay / UPI)
- [ ] Real-time order tracking
- [ ] Loyalty points and referral system
- [ ] Multi-language support (Hindi / English)
- [ ] Admin panel for service providers

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add my feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Arush Garg**  
[![GitHub](https://img.shields.io/badge/GitHub-@ArushGarg-181717?logo=github)](https://github.com/your-username)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Arush%20Garg-0077B5?logo=linkedin)](https://linkedin.com/in/your-profile)

---

<p align="center">Made with ❤️ using Flutter & Firebase</p>
