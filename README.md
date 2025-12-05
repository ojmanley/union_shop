# Union Shop Flutter App

## Project Title and Description

**Union Shop** is a Flutter mobile application for the University of Portsmouth's union shop. It provides students and staff with a seamless way to browse, explore, and purchase university-branded products and merchandise.

### Key Features

- **Home Page**: Features promotional banners, hero sections, and a product showcase grid
- **Product Catalog**: Browse individual products with detailed information and pricing
- **Collections**: Explore curated product collections
- **Sales Section**: View current promotions and discounted items
- **Print Shack**: Customize and order personalized hoodies with one or two lines of custom text
  - Dynamic pricing: £15 for one line, £20 for two lines
  - Text input fields that adapt based on selected line count
- **Shopping Cart**: Add and manage items for purchase
- **User Authentication**: Sign-in page for user accounts
- **About Section**: Learn more about the union shop
- **Navigation Drawer**: Easy access to all major sections from any page
- **Responsive Design**: Optimized layouts for different screen sizes

---

## Installation and Setup Instructions

### Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Flutter SDK** (version 2.17.0 or higher)
  - [Install Flutter](https://flutter.dev/docs/get-started/install)
- **Dart SDK** (included with Flutter)
- **Android Studio** or **Xcode** (for running on emulators/devices)
  - Android Studio for Android development
  - Xcode for iOS development (macOS only)
- **Git** (for cloning the repository)

### Clone the Repository

```bash
git clone https://github.com/ojmanley/union_shop.git
cd union_shop
```

### Step-by-Step Installation Guide

1. **Install Flutter dependencies**:
   ```bash
   flutter pub get
   ```

2. **Verify Flutter setup** (optional but recommended):
   ```bash
   flutter doctor
   ```
   This command checks your environment and displays a report of the status of your Flutter installation.

3. **Set up an emulator or connect a device**:
   - **Android**: Start an Android emulator using Android Studio or connect a physical Android device
   - **iOS**: Start an iOS simulator or connect a physical iOS device (macOS only)

### How to Run the Project

1. **Run the app in debug mode**:
   ```bash
   flutter run
   ```

2. **Run the app in release mode** (for production):
   ```bash
   flutter run --release
   ```

3. **Run on a specific device** (if multiple devices are available):
   ```bash
   flutter devices  # List available devices
   flutter run -d <device_id>
   ```

4. **Run tests**:
   ```bash
   flutter test
   ```

---

## Usage Instructions

### Main Navigation

The app uses a **drawer menu** accessible from any page via the menu icon (☰) in the header. The menu provides quick access to:

- **Home**: Returns to the main home screen
- **Products**: Browse the full product catalog
- **Collections**: View curated product collections
- **Sale**: See current promotions and discounts
- **About**: Learn about the union shop
- **Sign In**: Access user authentication
- **Cart**: View your shopping cart
- **Print Shack**: Customize personalized products

### Key User Flows

#### 1. **Browsing Products**
   - Start at the **Home Screen** to see featured products
   - Tap any product card to view detailed product information on the **Product Page**
   - Use the **drawer menu** to navigate to specific sections (Collections, Sale, etc.)

#### 2. **Shopping Cart**
   - Browse products across different sections
   - Add items to your cart via the cart icon in the header (functionality to be implemented)
   - Navigate to **Cart** from the drawer menu to review your items

#### 3. **Using Print Shack (Personalized Hoodies)**
   - Open the drawer and select **Print Shack**
   - Choose the number of text lines:
     - **One Line**: £15.00
     - **Two Lines**: £20.00
   - Enter your custom text in the provided text field(s)
   - The price updates automatically based on your selection
   - Proceed to add to cart or checkout

#### 4. **Exploring Collections**
   - From the drawer, select **Collections** to see all available product collections
   - Tap on a specific collection to view its products
   - Each collection showcases related items grouped by theme or category

#### 5. **Viewing Sale Items**
   - Select **Sale** from the drawer to see discounted items
   - Current promotion: Essential range at 20% off

#### 6. **User Account**
   - Navigate to **Sign In** from the drawer to access or create an account
   - (Account functionality to be implemented by students)

### App Structure

The app is organized into the following main pages:

```
lib/
├── main.dart                 # App entry point and routing
├── home_page (main.dart)     # Home screen with featured products
├── product_page.dart         # Individual product details
├── collections_page.dart     # All collections listing
├── collection_page.dart      # Single collection view
├── sale_page.dart            # Sale/promotion items
├── about_page.dart           # About union shop
├── signin_page.dart          # User authentication
├── cart_page.dart            # Shopping cart
└── printshack_page.dart      # Personalized hoodie customization
```

### Header Navigation

All pages feature a consistent header with:
- **Union Shop Logo** (top left) - Clickable to return home
- **Search Icon** - For product search (placeholder)
- **Person Icon** - For user account access (placeholder)
- **Shopping Bag Icon** - Quick access to cart (placeholder)
- **Menu Icon** (☰) - Opens the navigation drawer

### Responsive Design

The app is designed to work seamlessly on:
- Small mobile devices (320px and up)
- Tablets and larger screens
- The product grid automatically adjusts from 1 column on mobile to 2 columns on larger screens

---

## Configuration Options

### Theme Customization

The app uses a custom color scheme with a primary color of **#4d2963** (deep purple). To customize:

1. Open `lib/main.dart`
2. Modify the `ThemeData` in the `UnionShopApp` class:
   ```dart
   theme: ThemeData(
     colorScheme: ColorScheme.fromSeed(seedColor: const Color(0xFF4d2963)),
   ),
   ```

### Adding New Pages

To add a new page to the app:

1. Create a new Dart file in `lib/` (e.g., `new_page.dart`)
2. Implement the page as a `StatefulWidget` with a drawer
3. Import it in `main.dart`
4. Add a route in the `routes` map of `UnionShopApp`
5. Add a navigation method to pages that need to access it
6. Add a `ListTile` to the drawer in all existing pages

### Modifying Print Shack Options

To adjust pricing or options for the Print Shack:

1. Open `lib/printshack_page.dart`
2. Modify the price calculation in the `Text` widget displaying the price
3. Adjust dropdown options or text field parameters as needed

---

## Testing

The project includes unit and widget tests. Run them with:

```bash
flutter test
```

Tests are located in the `test/` directory and cover:
- Home page UI elements
- Product page functionality
- Icon and text rendering

---

## Troubleshooting

### Common Issues

1. **"Flutter command not found"**: Ensure Flutter is added to your system PATH
2. **Emulator won't start**: Try restarting Android Studio or Xcode
3. **Dependencies not installing**: Run `flutter clean` followed by `flutter pub get`
4. **Network image errors in tests**: Tests mock network calls; physical device tests may differ

---

## Future Enhancements

- Implement full shopping cart functionality
- Add user authentication backend integration
- Integrate payment processing
- Add product search and filtering
- Implement order history and tracking
- Add push notifications
- Enhance Print Shack with color/style options

---

## Contributing

To contribute to this project:

1. Create a new branch for your feature
2. Make your changes
3. Run tests to ensure everything works
4. Submit a pull request

---

## License

This project is part of the University of Portsmouth curriculum and is for educational purposes.

---

## Support

For issues or questions about the app, please contact the development team or open an issue in the repository.

---

**Last Updated**: December 5, 2025
