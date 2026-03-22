# Health Dashboard SwiftUI Project – Explanation

This project is a Health Dashboard app built in SwiftUI, designed to display and manage multiple users’ health data. It demonstrates state management, navigation, forms, and reusable UI components in SwiftUI.
#Key Features
User Data Model
UserHealth struct holds each user’s health metrics: name, heart rate, water intake, blood pressure, steps, and status.
Conforms to Identifiable for use in lists.
# Dashboard
Displays the current user’s health stats including heart rate, water intake, activity (steps), blood pressure, and status.
Includes HeartWaveView, a simple animated line graph for heart rate visualization.
Uses reusable cards (DashboardCard) for a clean, organized layout.
# User Management
AddUserView allows adding new users with a simple form.
UserListView shows all users in a scrollable list using UserCardView.
# Navigation
Uses NavigationStack and NavigationLink to move between the dashboard and user list.
Users can add new entries via a modal sheet.
# UI Design
Uses LazyVGrid for info cards, rounded corners, shadows, and system colors for a modern look.
HeartWaveView simulates heart rate visually.
# State Management
@State and @Binding ensure that adding a new user updates the dashboard and list in real time.
# Learning Points / AP CSP Relevance
Demonstrates data structures (arrays of structs) and state management.
Implements conditional UI updates with SwiftUI bindings.
Includes navigation and user interaction, key for app development.
Offers a modular structure: reusable views for cards, heart wave, and user list.
