Interactive Learning & Collaboration Platform: 

Custom NoSQL Authentication Demo

This project is a single-file HTML application demonstrating a custom user registration and sign-in flow using Firestore as a NoSQL database for credential storage, bypassing Firebase's built-in authentication services.

It features a basic multi-view interface (Dashboard, Feed, Discussions) that is accessible only after successful login.

🚀 How to Use the Application
Since this is a single .html file, you can run it directly in your browser or within the provided environment's preview pane.

1. Registration (Sign Up)
To create a new user account:

Click the "Need an account? Sign Up" button below the Sign In form.

The form title will change to "Register", and two fields will appear: Username and Role (Learner/Mentor).

Enter a valid Email Address and a Password (minimum 6 characters).

Enter your desired Username and select a Role.

Click the "Sign Up" button.

Upon successful registration, your profile data (including the plain-text password for demonstration purposes) is stored in the Firestore collection: artifacts/{appId}/public/data/users. You will be automatically logged in and taken to the Dashboard.

2. Sign In
To log in using a registered account:

Ensure the form is set to "Sign In" mode.

Enter the Email Address and Password you registered with.

Click the "Sign In" button.

The application queries Firestore to find a user document where the stored email and plain-text password match your input. If successful, you gain access to the main application view.

3. Application Navigation
Once logged in, you can navigate between the primary views:

Dashboard: Displays your welcome message, role, and simulated User ID (the Firestore document ID).

Feed: Shows mock content from other community members.

Discussions: A placeholder for future collaborative features.

Use the "Sign Out" button in the navigation bar to end your session.

🔒 Important Security Note
This application uses a simplified, client-side authentication model for demonstration purposes only.

DO NOT USE THIS CODE IN A PRODUCTION ENVIRONMENT.

In a real-world application, user passwords MUST be securely hashed and salted using a strong, one-way cryptographic function (like Argon2 or bcrypt) on a secure backend server or using a service like Firebase Authentication. Storing passwords in plain text in Firestore (as done here for simplicity) is a critical security vulnerability.
