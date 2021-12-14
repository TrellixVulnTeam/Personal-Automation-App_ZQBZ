How this automation folder works
========================
The main script that is being run constantly in the background is **app.pyw**
All the other python scripts in here are being imported and called in the main script.

### When making a new automation module:
1. Only use paths in var.py
2. Add an exclude parameter that takes in a list defaulted to an empty list.
3. Make sure to use the logging module

### When adding anything to the main script:
1. Make a new subclass of FileSystemEventHandler.
3. Describe clearly what the script does as a comment in the main script.

### To end the automation app:
1. Open Command Line
2. Enter this command ```wmic process where caption="wscript.exe" get commandline,processid```
3. Make sure it is the right task
4. Enter this command ```taskkill /F /PID {The tasks's PID}```
