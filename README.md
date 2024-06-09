# Celebrity-details-website
Introduction
The Celebrity Details website is a full-stack web application designed to provide users with detailed information about various celebrities. The application leverages both frontend and backend technologies to deliver a seamless and interactive experience. Here is a comprehensive description of how the application is structured and operates:

Frontend
The frontend of the application is responsible for the user interface and interaction. It is built using HTML, CSS, and JavaScript, with EJS (Embedded JavaScript) templating for rendering dynamic content.

Key Features:
Home Page: The landing page provides an overview of the website and navigation links to other sections.
Login and Signup Pages: Forms for user authentication, allowing users to create accounts and log in to access personalized features.
Dashboard: Once logged in, users are taken to their dashboard, where they can search for celebrity information.
Celebrity Search Form: A form where users can enter the name of a celebrity to fetch their details.
Celebrity Details Table: Displays the fetched celebrity information in a tabular format.
Backend
The backend of the application is built using Node.js with the Express framework. It handles user authentication, data fetching, and communication with the Firebase Firestore database.

Key Features:
User Authentication: Handles login and signup functionality using sessions to maintain user state.
Firestore Database: Stores user data securely, including hashed passwords for security.
Celebrity Data Fetching: Communicates with an external API (Ninja APIs) to fetch and return celebrity details based on user queries.
Endpoints:
/loginSubmit: Handles login form submissions.
/signupSubmit: Handles signup form submissions.
/dashboard: Serves the user dashboard after successful login.
/getCelebDetails: Fetches celebrity details from an external API and returns them to the frontend.
Full-Stack Interaction
User Authentication:

When a user signs up, their details are stored in the Firestore database with their password securely hashed.
During login, the provided credentials are verified against the stored hashed password, and if successful, a session is created for the user.
Fetching Celebrity Data:

The user enters a celebrity's name in the search form on the dashboard.
The frontend sends an AJAX request to the backend endpoint /getCelebDetails with the celebrity's name as a query parameter.
The backend processes this request by making an HTTP request to the external API.
Upon receiving the data from the external API, the backend sends this data back to the frontend.
The frontend then dynamically updates the table with the fetched celebrity details.
