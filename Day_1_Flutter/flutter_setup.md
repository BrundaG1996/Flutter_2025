Creating a New Flutter Project in VS Code on Ubuntu
Method 1: From VS Code (Recommended)
1. Open VS Code.
2. Press: Ctrl + Shift + P
3. In the search box, type: Flutter: New Project
4. Select: Application
5. Choose a folder where you want to save the project.
6. Enter your project name (e.g. my_first_flutter_app).
7. Wait for dependencies to be fetched.
8. Open the lib/main.dart file — this is your starting point.
Method 2: From Terminal
1. Open a terminal (VS Code or normal Ubuntu terminal).
2. Go to the folder where you want the project:
   cd ~/Desktop
3. Create a new Flutter project:
   flutter create my_first_flutter_app
4. Go into the project folder:
   cd my_first_flutter_app
5. Open it in VS Code:
   code .
Run Your New Project in Chrome
1. Enable web support (only once):
   flutter config --enable-web
2. Run in Chrome:
   flutter run -d chrome
Fixing Flutter Command Not Found in VS Code Terminal
If Flutter works in your normal Ubuntu terminal but not in VS Code's integrated terminal, follow these steps:
1️⃣ Open the correct JSON file
In VS Code, press: Ctrl + Shift + P
Type: Preferences: Open User Settings (JSON)
→ Pick the one that says 'User'.
2️⃣ Add this line
Inside the { ... } JSON object, add:
"terminal.integrated.inheritEnv": true
Example:
{
    "terminal.integrated.inheritEnv": true
}
3️⃣ Save & Restart VS Code
Press Ctrl + S
Close VS Code completely
Reopen it.
4️⃣ Test
Open the VS Code terminal (Ctrl + `) and run:
flutter --version
If it works → now run:
flutter run -d chrome
💡 If you want, you can skip this setting change and instead use a quick one-line fix to make Flutter work in VS Code terminal without changing any settings.
