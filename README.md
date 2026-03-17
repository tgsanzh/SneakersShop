# 👟 SneakersShop

SneakersShop is an Android e-commerce app for browsing sneakers, adding items to a cart, and placing orders.

The project is built with **Kotlin**, **Jetpack Compose**, **Fragments + Navigation Component**, and **Room**, and demonstrates a simple event-driven UI architecture with local persistence.

---

## Features

* User registration and login
* Local session persistence with `SharedPreferences`
* Sneakers catalog screen
* Add products to cart
* Increase and decrease item quantity in cart
* Create orders from cart items
* View order history
* View order details
* Profile screen with sign out

---

## Tech Stack

* **Kotlin**
* **Jetpack Compose**
* **Android Fragments**
* **Navigation Component**
* **Room Database**
* **KSP**
* **Material 3**

---

## Architecture Overview

The app uses a layered structure centered around:

* **UI screens built with Jetpack Compose**
* **Fragments as navigation containers**
* **ViewModels with `State` + `Event` pattern**
* **Room for local data storage**

Project structure:

```text
app/src/main/java/com/example/sneakersshop/
├── Fragments/
│   ├── Authorization/
│   ├── Login/
│   ├── Catalog/
│   ├── Cart/
│   ├── Profile/
│   ├── Orders/
│   └── OrderDetail/
├── Model/
│   ├── DAO/
│   ├── Entity/
│   ├── AppDatabase
│   └── DatabaseProvider
├── ui/theme/
├── CurrentUserData.kt
└── MainActivity.kt
```

---

## Data Layer

The app stores data locally using Room.

### Entities

* `User`
* `Boot`
* `Cart`
* `Order`

### DAO interfaces

* `UserDao`
* `BootDao`
* `CartDao`
* `OrderDao`

The catalog is seeded locally on first launch if the sneaker table is empty.

---

## Navigation Flow

* **Login**
* **Authorization**
* **Catalog**
* **Cart**
* **Profile**
* **Orders**
* **Order Details**

Navigation is implemented with the **Navigation Component** using a single `nav_graph.xml`.

---

## How It Works

* Users can sign up and log in
* The authenticated user is stored locally
* Sneakers are loaded from the local Room database
* Products can be added to the cart
* Cart items can be updated by changing quantity
* When checkout is triggered, a new order is created and cart items are linked to that order
* Users can view previous orders and open detailed order information

---

## Getting Started

### Requirements

* Android Studio
* Android SDK 24+
* JDK 8+

### Run locally

```bash
git clone https://github.com/tgsanzh/SneakersShop.git
cd SneakersShop
```

Then open the project in **Android Studio** and run it on an emulator or physical Android device.

---

## Build Configuration

* **Min SDK:** 24
* **Target SDK:** 34
* **Compile SDK:** 35

---

## Dependencies

Main libraries used in the project:

* `androidx.compose`
* `androidx.navigation`
* `androidx.room`
* `androidx.lifecycle`
* `androidx.activity.compose`

---

## Purpose of the Project

This project was created to practice and demonstrate:

* Android app architecture
* Compose-based UI development
* Local persistence with Room
* Navigation between multiple screens
* Basic e-commerce flow implementation

---

## Future Improvements

* Product search and filtering
* Better state handling for async loading
* Dependency injection
* Unit tests
* UI tests
* Remote API integration
* Better validation and error handling

---

## Author

**Sanzhar Tursynbay**
