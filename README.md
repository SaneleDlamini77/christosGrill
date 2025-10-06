Christo’s Grill – Digital Menu Management App (Part 2)
Student: Sanele Dlamini
Student Number: ST10172088
Module: Mobile App Scripting (MAST5112)
Portfolio of Evidence: Part 2
Year: 2025
📱 Project Overview

Christo’s Grill is a React Native + TypeScript mobile application that allows a restaurant chef to manage and display menu items dynamically.
This project demonstrates the use of React Navigation, state management, animations, and TypeScript programming logic to create an interactive, user-friendly interface.

The app is developed for Part 2 of the Portfolio of Evidence, expanding upon the previous wireframes and report from Part 1.

🎯 Learning Outcomes

By completing this project, the student is able to:

✅ Create a fully featured user interface using React Native components

✅ Use layouts and color schemes effectively

✅ Handle text input and button presses

✅ Use TypeScript variables and logic to store and manipulate data

✅ Navigate between multiple screens using React Navigation

✅ Apply animations to improve user experience

✅ Use if statements and loops to solve programming problems

✅ Display and count menu items dynamically

🧩 App Features
👨‍🍳 Chef Menu Management

Add new menu items with:

Dish Name

Description

Course (Starter, Main, Dessert)

Price

Input validation ensures all fields are filled before submission.

🏠 Home Screen

Displays all added menu items dynamically.

Shows the total number of available dishes.

Allows the chef to navigate to the “Add Menu Item” screen.

➕ Add Menu Item Screen

Input form for dish details.

Dropdown for selecting a course.

“Add Item” button saves data using useState.

🧭 Navigation

Uses React Navigation Stack for smooth screen transitions.

Screens:

Home

Add Menu Item

Filter Menu

Menu Selection

Final Menu Display

💫 Animations

Fade-in effect when new items are added.

Smooth transitions between screens.

🧮 Dynamic Data Handling

Menu data stored temporarily using React state (useState).

No hardcoded or permanent data storage required.

🧱 Technologies Used
Tool / Library	Purpose
React Native (Expo)	Cross-platform development
TypeScript	Type-safe programming
React Navigation	Multi-screen navigation
React Hooks (useState, useEffect)	State management
Animated API	Simple fade animations
StyleSheet API	Consistent styling and layout
🧠 Programming Concepts Used
Concept	Example
Variables & State	useState<MenuItem[]>([])
If Statements	Checking empty inputs before adding items
Loops	Counting total menu items or calculating totals
Functions	handleAddItem() for adding new dishes
Navigation	navigation.navigate("AddMenuItem")
UI Components	View, Text, FlatList, TouchableOpacity, TextInput
🎨 Design Summary

Elegant restaurant branding: gold, black, and deep red

Clean and readable layout with spacing

Consistent text and button styles

Logo image displayed on Home Screen

Responsive layout using Flexbox

📂 File Structure
ChristosGrill/
├── App.tsx
├── types.ts
├── package.json
├── README.md
├── assets/
│   └── logo.png
└── screens/
    ├── HomeScreen.tsx
    ├── AddMenuItemScreen.tsx
    ├── FilterScreen.tsx
    ├── MenuSelectionScreen.tsx
    └── FinalMenuDisplay.tsx

⚙️ Installation & Setup Instructions
🪟 Prerequisites

Ensure you have the following installed:

Node.js (v18 or later)

npm or yarn

Expo CLI (npm install -g expo-cli)

Android Studio or Expo Go App (for testing)

🧩 Steps to Run the App

Clone the Repository

git clone https://github.com/<your-username>/ChristosGrill.git
cd ChristosGrill


Install Dependencies

npm install
# or
yarn install


Start the App

npx expo start


Run on Emulator or Phone

Press “a” to open Android Emulator

Scan the QR code in the terminal using Expo Go App on your mobile device

🧾 Example TypeScript Code (App Logic)
const [dishName, setDishName] = useState('');
const [description, setDescription] = useState('');
const [course, setCourse] = useState('Starter');
const [price, setPrice] = useState('');
const [menuItems, setMenuItems] = useState<MenuItem[]>([]);

const handleAddItem = () => {
  if (dishName && description && price) {
    setMenuItems([
      ...menuItems,
      { dishName, description, course, price: parseFloat(price) }
    ]);
    setDishName('');
    setDescription('');
    setCourse('Starter');
    setPrice('');
  } else {
    alert('Please fill in all fields');
  }
};

🎥 Demo Video

link: 

The video demonstrates:

Launching the app

Adding a new menu item

Viewing items on the home screen

Navigating between screens

🔗 GitHub Repository

📦 GitHub Repo:(https://github.com/SaneleDlamini77/christosGrill/edit/main/README.md)

🧩 Future Enhancements

Persistent storage using AsyncStorage or SQLite

User authentication for chefs

Improved animation with React Native Reanimated

Filtering and search functionality for large menus

🧾 References

Canva. (2025). Wireframe Design Resources.

The IIE. (2025). Mobile App Scripting Module Manual.

MindInventory. (2025). Wireframing in Mobile App Development.

Space-O Technologies. (2025). Creating Modern App Wireframes.

React Native Docs. (2025). Components, Navigation & TypeScript Integration.
