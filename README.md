# RBAC-SYSTEM-UI
Role-Based Access Control (RBAC) UI
This project is a Role-Based Access Control (RBAC) System designed with Firebase Authentication and Realtime Database integration. The system allows user management and access control based on roles such as Designer, Developer, Tester, Manager, and Admin.

Admins can manage security keys, while users can sign up, log in, and navigate to their respective role-based dashboards.

Features
Login System:

Users can log in using their email and password.
Admin has an additional security key verification layer.
Sign-Up System:

Users can sign up by providing a name, email, password, and selecting a role.
All new users require admin approval.
Role-Based Redirection:

Redirects users to role-specific dashboards (e.g., Developer.html, Tester.html).
Admin Security Key:

Admin access requires an additional Security Key.
Admin can update the Security Key securely.
Firebase Integration:

Firebase Authentication for login and sign-up.
Firebase Realtime Database for user data and role management.
Technologies Used
Frontend:
HTML5
CSS3
JavaScript (Vanilla)
Backend:
Firebase Authentication
Firebase Realtime Database
Deployment:
Compatible with any static web hosting service (e.g., Firebase Hosting, Netlify).
Project Structure
bash
Copy code
RBAC-UI/
├── index.html           # Main login/signup page
├── admin.html           # Admin dashboard (after login)
├── Developer.html       # Developer dashboard
├── Tester.html          # Tester dashboard
├── Designer.html        # Designer dashboard
├── Manager.html         # Manager dashboard
├── style.css            # Styles for the UI
├── app.js               # Frontend JavaScript logic
├── firebase.js          # Firebase configuration and initialization
└── README.md            # Documentation
Setup Instructions
1. Clone the Repository
bash
Copy code
git clone https://github.com/yourusername/RBAC-UI.git
cd RBAC-UI
2. Configure Firebase
Create a Firebase project in the Firebase Console.
Enable Authentication (Email/Password sign-in).
Set up Realtime Database with the following structure:
json
Copy code
{
  "users": {
    "uniqueUserId": {
      "name": "John Doe",
      "email": "john@example.com",
      "password": "hashed-password",
      "role": "Developer",
      "approved": "yes"
    }
  }
}
Copy your Firebase project configuration (API key, Auth domain, etc.) and paste it into firebase.js.
3. Host the App
You can host the app on Firebase Hosting, Netlify, or any static hosting service.
To host using Firebase:
bash
Copy code
firebase init
firebase deploy
How to Use
Admin Login
Enter the admin email (admin@gmail.com) and password (admin@12).
Input the Security Key for access (default or updated by the admin).
User Login
Enter your registered email and password.
Upon login, you'll be redirected to your role-based dashboard.
Sign-Up
Fill in your name, email, password, and select a role.
Wait for admin approval to gain access.
Changing Security Key
Admin can open the Change Security Key Modal.
Enter the current key and a new key.
Update the key securely through Firebase.
Screenshots
Login Page:
Simple and intuitive login form for both admin and users.
Sign-Up Page:
Easy form with role selection dropdown.
Role-Based Dashboards:
Users are redirected based on their roles.
Admin Security Key Modal:
Secure modal to update the admin key.
Future Enhancements
Add email notifications for approvals or rejections.
Enhance UI/UX for better accessibility and responsiveness.
Implement a detailed activity log for admin actions.
Contributing
Feel free to fork this repository and submit pull requests. Contributions are welcome!

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
Developer: Karan Tiwari
Email: coderlife404@gmail.com

Feel free to reach out for queries or collaboration opportunities!
