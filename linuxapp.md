# Linux App with customtkinter


## Setting Up

- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo apt install python3-tk -y</button> on system Install tkinter
- <button onclick="navigator.clipboard.writeText(this.innerText)">pip install customtkinter</button> Inside venv Install customtkinter
  
## Build the Python App


import customtkinter as ctk

import subprocess

ctk.set_appearance_mode("dark")

ctk.set_default_color_theme("green")

app = ctk.CTk()

app.title("Control Panel")

app.geometry("400x400")

title = ctk.CTkLabel(app, text="Clash Controls", font=("Arial", 20)).pack(pady=10)

btn1 = ctk.CTkButton(app, text="Restart Clash", command=lambda: subprocess.run(["pkexec", "systemctl", "restart", "clash"])).pack(pady=10)

app.mainloop()

## Create Launcher Script

- <button onclick="navigator.clipboard.writeText(this.innerText)">nano run.sh</button> 
  
#!/bin/bash

source /home/danny/Documents/2_Projects/DesktopApp/venv/bin/activate

python3 /home/danny/Documents/2_Projects/DesktopApp/MonitorApp.py

- <button onclick="navigator.clipboard.writeText(this.innerText)">chmod +x run.sh</button> Make it Executable

## Create Desktop App

- <button onclick="navigator.clipboard.writeText(this.innerText)">nano ~/.local/share/applications/MonitorApp.desktop</button> 

[Desktop Entry]

Name=Control Panel

Comment=Manage local services

Exec=/home/danny/Documents/2_Projects/DesktopApp/run.sh

Icon=/home/danny/Documents/2_Projects/DesktopApp/icon.png

Terminal=false

Type=Application

Categories=Utility;


- <button onclick="navigator.clipboard.writeText(this.innerText)">chmod +x ~/.local/share/applications/MonitorApp.desktop</button> Enable it
- <button onclick="navigator.clipboard.writeText(this.innerText)">update-desktop-database ~/.local/share/applications</button> Refresh the app list