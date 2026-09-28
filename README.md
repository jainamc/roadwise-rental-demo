# Roadwise Vehicle Rental Demo

Roadwise has two versions:

- `index.html`: standalone browser app. No install or web server is required.
- `.vscode/oops.cpp`: C++ console version. Compile it with a C++17 compiler such as MinGW g++.

## Run on this computer

Open `index.html` in a browser, or from PowerShell in this folder run:

```powershell
Start-Process .\index.html
```

In VS Code, press `Ctrl+Shift+P`, choose `Tasks: Run Task`, then run `Open Rental Web App` or `Run Rental System (C++)`.

To build and run the C++ version manually:

```powershell
g++ -std=c++17 -Wall -Wextra -pedantic .vscode\oops.cpp -o .vscode\oops.exe
.\.vscode\oops.exe
```

## Share the browser demo

For a quick handoff, send `index.html`. The other person can download it and open it in a browser. Internet access is needed for the remote vehicle photos and web fonts; the app itself is local.

For a stable link that works on phones and computers:

1. Create a GitHub repository for this project.
2. Upload `index.html` and this `README.md`. You can also include `.vscode/oops.cpp` and `.vscode/tasks.json` to share the source and VS Code tasks.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose the `main` branch and `/ (root)`, then save.
5. Wait for the Pages address shown there, usually `https://YOUR-USER.github.io/REPOSITORY/`, and send that link.

The HTML app saves changes in each browser's local storage. Each person gets a separate copy of the demo data; it does not synchronize bookings between users. A shared live rental system needs a hosted backend and database, plus user accounts and server-side booking conflict checks. Do not use the current demo to store real customer information or take payments.

## Share the C++ console version

Share `.vscode/oops.cpp` with the recipient. They need a C++17 compiler installed. On Windows with MinGW g++, they can run the build commands above from the project folder. VS Code tasks are optional and only work when opening the whole project folder in VS Code.