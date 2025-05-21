# EEP Communication Portal App (Frontend)

This repository contains the source code for the EEP Communication Portal application. This application is designed to serve as a central platform for communication and information management within Ethiopian Electric Power (EEP).

## Overview

The EEP Communication Portal is a web application that provides various functionalities based on user roles. It features modules for managing news articles, media monitoring, tasks, and employee information, as well as generating reports. The application is built using React for the frontend and includes server-side logic for handling API requests and interacting with MYSQL database.

## Features


*   **User Authentication Flow:** Provides a `LoginForm` component for users to enter their username and password. After successful login (handled by interaction with a backend), user details like username, role, and ID are stored in `localStorage` for session management.
*   **Role-Based Views:** The application dynamically renders different content and navigation options based on the logged-in user's role.
    *   **Navigation/Sidebar:** A sidebar menu provides links to different sections. Access to "Dashboard/Reports" and "Employee" (Settings) is restricted to users with roles like "CEO", "Director", "Manager", or "Admin". The "Tasks" view is accessible to all logged-in users.
    *   **Content Area:** The main area renders the content based on the selected view (e.g., `NewsArticleTab`, `MediaMonitoringTab`, `TaskDashboard`). An "Access Denied" message is shown if a user tries to access restricted views like "Report" or "Setting" without the appropriate role.
*   **Navigation:** Sidebar navigation for accessing different sections like Feeds, News Article, Media Monitoring, Report, Tasks, and Employee (Settings).
*   **User Profile:** Includes a `ProfileTab` component to display the currently logged-in user's details.
*   **Logout Functionality:** A logout option is available in a dropdown menu accessed from the top bar. This clears the user data from `localStorage` and returns the user to the login screen.
*   **Dropdown Menu:** A dropdown menu in the top bar provides access to "Profile Detail" and "Logout". The dropdown visibility is managed using React state (`isDropdownOpen`) and references (`useRef`) to handle clicks outside the menu.
*   **Styling:** Custom branding colors are defined using `BRAND_COLORS` constants. The UI uses a combination of React inline styles and CSS classes defined separately. Basic media queries are included in the CSS to adjust the layout for smaller screens, such as stacking the sidebar and main content vertically.

## Setup and Running

## Technologies

*   React
*   ReactDOM
*   JavaScript (ES Modules)
*   CSS

## License

**Solomon Ferede** – [ezezsolomonferede@gmail.com](mailto:ezezsolomonferede@gmail.com) / [solomonf1227@gmail.com](mailto:solomonf1227@gmail.com)

