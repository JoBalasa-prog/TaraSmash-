# TaraSmash! Court Monitor

## Business Name & Description
**Business Name:** TaraSmash! Courts[cite: 10]
**Description:** TaraSmash! is a local badminton facility offering court rentals to sports enthusiasts. This system is a real-time booking and facility management web application[cite: 10]. It is used by **customers (players)** to check real-time court availability and reserve time slots, and by the **facility administrator** to monitor court usage, manage reservations, and provide customer support[cite: 10].

## Problem Being Solved
Manual court booking systems (like pen-and-paper or basic spreadsheets) are prone to double-booking, require constant manual updates, and lack a streamlined way for customers to communicate with staff[cite: 10]. This system solves these issues by providing a centralized, real-time dashboard where availability is instantly synced across all users, pricing is calculated automatically, and customers can privately chat with the admin for immediate assistance.

## Feature List
*   **Landing Page (Dashboard):** A responsive, interactive grid displaying real-time availability for 9 courts across a 13-hour schedule (08:00 AM - 09:00 PM)[cite: 10]. Includes dynamic color-coding (Available, Booked, Void/Maint) and auto-calculating price indicators based on duration.
*   **Users:** Dual-role architecture supporting an Admin mode and a standard User (Customer) mode, managed via a modal interface[cite: 10].
*   **CRUD Functionality:**[cite: 10]
    *   **Create:** Users can create court bookings (single or multi-hour) with specified payment methods (GCash/Cash). Users and Admins can create chat messages.
    *   **Read:** The system continuously reads and displays live booking statuses and real-time chat histories from the database.
    *   **Update:** Admins can update court statuses (overriding bookings or setting courts to maintenance).
    *   **Delete:** Admins can void/delete existing customer bookings directly from the dashboard.
*   **Live Private Chat:** 1-on-1 real-time messaging between customers and the admin, featuring audio chimes, visual notification badges, and a global chat listener for the admin to manage multiple customer inquiries simultaneously.

## Tech Stack Used
*   **Frontend:** HTML5, Vanilla JavaScript, Tailwind CSS (via CDN for rapid UI development)[cite: 10].
*   **Backend/Database:** Firebase (Cloud Firestore) for real-time NoSQL data synchronization across all clients[cite: 10].
*   **Hosting:** Netlify (for live deployment).

## Setup and Run Instructions
To run this project from a clean machine:[cite: 10]

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/tarasmash-court-monitor.git](https://github.com/yourusername/tarasmash-court-monitor.git)
    cd tarasmash-court-monitor
    ```
2.  **Firebase Configuration:**
    *   The project relies on Firebase Firestore. The `index.html` file contains a `firebaseConfig` object. 
    *   Ensure the provided API keys in the script tag are active, or replace them with your own Firebase project credentials to link it to your own database.
3.  **Run Locally:**
    *   Because it uses ES modules and external CDNs, it is best to run it through a local web server to avoid CORS issues.
    *   If you have Python installed, run: `python -m http.server 8000`
    *   Alternatively, use the "Live Server" extension in VS Code.
4.  **Access the Application:**
    *   Open your web browser and navigate to `http://localhost:8000` (or the port provided by your local server).

## AI Tools Used
*   **Gemini:** Used extensively as an AI pair-programmer to generate the core HTML structure, implement Tailwind CSS styling, write the Vanilla JavaScript logic for the UI, and integrate Firebase Firestore for real-time database operations[cite: 10]. It was also used to debug authentication errors, transition from Firebase Auth to a hardcoded client-side role system, and implement complex features like the global chat listener and multi-hour pricing calculator[cite: 10].

## Test Accounts
To access the system, click the "Login" button in the top navigation bar and select the appropriate tab.[cite: 10]

*   **Admin Account:**[cite: 10]
    *   **Username:** `Admin` (case-sensitive)
    *   **Password:** `Admin` (case-sensitive)
*   **Regular User Account:**[cite: 10]
    *   **Username:** Any name (e.g., `Juan`, `Maria`, `Customer1`)
    *   **Password:** Any password (the system allows unrestricted entry for standard users to facilitate easy booking testing).
