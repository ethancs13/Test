# Setting Up a Local Development Environment for Web Development

## Introduction

### Purpose
This guide will help you set up a complete local development environment for web development on your computer. A local development environment allows you to build, test, and debug websites on your own machine before deploying them to the internet. This is an essential skill for computer science students and web developers.

### Who This Guide Is For
This guide is designed for **novice developers** who are new to web development. No prior experience with development tools is required—just basic computer skills and the ability to follow step-by-step instructions.

### What You'll Need
- A computer running Windows 10/11, macOS, or Linux
- Administrator access to install software
- Stable internet connection for downloading tools
- Approximately 2-3 hours to complete the setup

### What You'll Accomplish
By the end of this guide, you will have:
- A code editor (Visual Studio Code) installed and configured
- Node.js and npm (package manager) installed
- Git version control system set up
- A local web server running
- Your first project created and viewable in a browser

---

## Step 1: Install Visual Studio Code

Visual Studio Code (VS Code) is a free, powerful code editor that will be your primary tool for writing code.

### 1.1 Download VS Code
Navigate to [https://code.visualstudio.com](https://code.visualstudio.com) and click the download button for your operating system.

<img width="1867" alt="VSCode1" src="https://github.com/user-attachments/assets/c5269451-7d3d-4b27-8ff8-ce7e4fff6f27" />

### 1.2 Run the Installer
- **Windows**: Double-click the downloaded `.exe` file and follow the installation wizard. Check "Add to PATH" during installation.
- **macOS**: Open the downloaded `.dmg` file and drag VS Code to your Applications folder.
- **Linux**: Follow the distribution-specific instructions on the download page.

### 1.3 Launch VS Code
Open VS Code from your applications menu or by typing `code` in your terminal (if added to PATH).

<img width="1867" alt="welcome-page" src="https://github.com/user-attachments/assets/66e1a772-5b54-4851-a74c-60e1e0b08659" />

### 1.4 Install Essential Extensions
Click the Extensions icon in the left sidebar (or press `Ctrl+Shift+X` / `Cmd+Shift+X`) and install:
- **Live Server**: Launches a local development server with live reload
- **Prettier**: Code formatter for consistent styling
- **ESLint**: JavaScript linting tool

---

## Step 2: Install Node.js and npm

Node.js is a JavaScript runtime that allows you to run JavaScript on your computer. npm (Node Package Manager) comes bundled with Node.js and helps you install development tools and libraries.

### 2.1 Download Node.js
Visit [https://nodejs.org](https://nodejs.org) and download the **LTS (Long Term Support)** version for your operating system.

<img width="1867" height="910" alt="image" src="https://github.com/user-attachments/assets/24db7238-a205-44c6-afa5-21820a898b3c" />

### 2.2 Install Node.js
Run the downloaded installer and follow these steps:
- Accept the license agreement
- Keep the default installation location
- Ensure "Add to PATH" is checked
- Complete the installation

### 2.3 Verify Installation
Open a new terminal or command prompt and type:
```bash
node --version
npm --version
```

You should see version numbers displayed for both commands. If you see errors, restart your computer and try again.

<img width="1867" alt="NPM" src="https://github.com/user-attachments/assets/fc772b86-3c2c-4de2-be7a-d6eaed942588" />


---

## Step 3: Install and Configure Git

Git is a version control system that tracks changes to your code and enables collaboration with other developers.

### 3.1 Download Git
Visit [https://git-scm.com/downloads](https://git-scm.com/downloads) and download Git for your operating system.

### 3.2 Install Git
- **Windows**: Run the installer and use default settings. Select "Git from the command line and also from 3rd-party software" when prompted.
- **macOS**: Install via the downloaded package or use Homebrew: `brew install git`
- **Linux**: Use your package manager: `sudo apt install git` (Ubuntu/Debian) or `sudo yum install git` (Fedora)

### 3.3 Configure Git
Open your terminal and set your name and email (these will be attached to your commits):
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 3.4 Verify Git Installation
Type `git --version` in your terminal. You should see the installed Git version.

---

## Step 4: Create Your First Web Project

Now that your tools are installed, create a simple web project to test your setup.

### 4.1 Create Project Directory
Open VS Code and create a new folder for your project:
- Click `File > Open Folder`
- Create a new folder named `my-first-website`
- Select this folder to open it in VS Code

### 4.2 Create Project Files
In VS Code's file explorer (left sidebar), create these new files by clicking the "New File" icon:

**index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Welcome to My Website!</h1>
    <p>This is my local development environment.</p>
    <button id="myButton">Click Me!</button>
    <script src="script.js"></script>
</body>
</html>
```

**style.css**
```css
body {
    font-family: Arial, sans-serif;
    max-width: 800px;
    margin: 50px auto;
    padding: 20px;
    background-color: #f0f0f0;
}

h1 {
    color: #333;
}

button {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
```

**script.js**
```javascript
document.getElementById('myButton').addEventListener('click', function() {
    alert('Your development environment is working!');
});
```

![folder-structure-intro](https://github.com/user-attachments/assets/76eba7b9-2c1f-4ed0-b488-443ddf245d59)


---

## Step 5: Run Your Local Web Server

### 5.1 Start Live Server
Right-click on `index.html` in the VS Code file explorer and select **"Open with Live Server"**.

Your default browser will automatically open and display your website at `http://127.0.0.1:5500` (or similar).

### 5.2 Test Your Website
- Verify the heading and paragraph are displayed
- Click the "Click Me!" button
- You should see an alert message confirming your environment works

### 5.3 Test Live Reload
Make a change to your HTML file (e.g., change the heading text) and save. Your browser should automatically refresh and show the changes—no manual refresh needed!

---

## Conclusion

### What Success Looks Like
You have successfully set up your local development environment if:
- ✅ VS Code opens and displays your project files
- ✅ Running `node --version` and `git --version` in terminal shows version numbers
- ✅ Your website displays in the browser when using Live Server
- ✅ Clicking the button shows an alert message
- ✅ Changes to your files automatically refresh in the browser

### Next Steps
Now that your environment is ready, you can:
- Learn HTML, CSS, and JavaScript fundamentals
- Install additional npm packages for your projects
- Initialize a Git repository (`git init`) to track your changes
- Explore VS Code keyboard shortcuts to code faster

---

## Tips and Troubleshooting

### Tips for Success
- **Keep your tools updated**: Periodically check for updates to VS Code, Node.js, and Git
- **Use keyboard shortcuts**: Learn VS Code shortcuts to work more efficiently
- **Organize your projects**: Create a dedicated folder (e.g., `Documents/Projects`) for all development work
- **Back up your work**: Use Git to commit changes regularly

### Common Issues and Solutions

**Problem**: Command not found after installation
- **Solution**: Restart your terminal or computer. Ensure the tool was added to PATH during installation.

**Problem**: Live Server doesn't launch the browser
- **Solution**: Check that the Live Server extension is installed. Try right-clicking the HTML file again, or click "Go Live" in the VS Code status bar.

**Problem**: Node.js installation fails
- **Solution**: Ensure you have administrator privileges. Try downloading the installer again or use a package manager like Homebrew (macOS) or Chocolatey (Windows).

**Problem**: Git commands don't work
- **Solution**: Verify Git is installed with `git --version`. If not found, add Git to your system PATH manually.

**Problem**: Port 5500 already in use
- **Solution**: Another application is using that port. Close other local servers or change the Live Server port in VS Code settings.

### Variations

**Alternative Code Editors**:
- **Sublime Text**: Lightweight alternative to VS Code
- **Atom**: Similar features to VS Code, developed by GitHub
- **WebStorm**: Professional IDE with advanced features (paid)

**Alternative Local Servers**:
- **Python HTTP Server**: Run `python -m http.server` in your project folder
- **Node.js http-server**: Install globally with `npm install -g http-server`

**For Advanced Users**:
- Set up a full development stack with database (MongoDB, PostgreSQL)
- Configure Docker containers for consistent environments
- Use version control platforms like GitHub or GitLab
