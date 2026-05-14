# fukui-kanko-hack

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

An iOS point-of-sale (POS) app for stores, named "ミケツ" (Miketsu). It allows store staff to log in, enter a payment amount, and process the transaction by scanning a customer's QR code. The app is built with Swift 5, using VIPER architecture and the Combine framework, with Firebase for backend services.

## Key Screens

-   **Login:** A simple login screen for store staff using an email and password.
-   **Payment:** After logging in, the main screen allows the user to input a payment amount.
-   **QR Scanner:** A camera view is presented to scan the customer's QR code, which contains their user information for the transaction.
-   **Confirmation:** A success alert is shown with a cash register sound upon successful payment.

## Features

-   **Store Authentication:** Secure login and logout for store accounts using Firebase Authentication.
-   **QR Code Payment:** Initiates payments by scanning a customer's QR code containing their user data.
-   **Transaction Logging:** Records payment history for each store in a dedicated Firestore collection.
-   **Modern Architecture:** Built with a clean VIPER architecture, separating concerns for better maintainability.
-   **Reactive Programming:** Utilizes the Combine framework for handling asynchronous events and data flows.

## Technology Stack

-   **Language:** Swift 5
-   **Architecture:** VIPER
-   **Frameworks:** UIKit, Combine, AVFoundation
-   **Backend:** Firebase Authentication, Firebase Firestore
-   **Dependency Management:** CocoaPods

## Requirements

-   Xcode 12 or later
-   CocoaPods 1.11.3 or later

## Getting Started

1.  **Firebase Setup:** Create a project in the [Firebase Console](https://console.firebase.google.com/). Enable Email/Password authentication and set up Firestore.
2.  **Configuration:** Download the `GoogleService-Info.plist` file from your Firebase project settings and place it in the `f-kanko/` directory.
3.  **Install Dependencies:** Open your terminal, navigate to the project's root directory, and run:
    ```bash
    pod install
    ```
4.  **Build & Run:** Open the generated `f-kanko.xcworkspace` file in Xcode and run the project.
5.  **Login:** The app includes hardcoded test credentials for demonstration. Use the following to log in:
    -   **Email:** `teststore@localhost.com`
    -   **Password:** `teststore`

## License

MIT License — see [LICENSE](LICENSE).