# Keylogger

- Developed a Keylogger using the pynput library in Python to capture and log keyboard input, saving it to a log.txt file.
- Explored basic field of Cybersecurity.

## Project Description

A basic implementation of a keylogger using the `pynput` library, which allows monitoring and controlling input devices. Here's how it works:

1. Importing Libraries: The script imports the necessary modules from `pynput.keyboard`. This library allows the script to monitor keyboard events.
2. Global Variables: `count` and `keys` are declared as global variables. `count` keeps track of the number of keystrokes captured, and `keys` is a list that stores the pressed keys.
3. `on_press` Function: This function is called whenever a key is pressed. It appends the pressed key to the `keys` list and increments the `count`. If `count` reaches 10 (indicating that 10 keys have been pressed), it calls the `write_file` function to write the captured keys to the log file and resets `count` and `keys`.
4. `write_file` Function: This function writes the captured keys to a file named "log.txt". It iterates over the `keys` list, converts each key to a string, and writes it to the file. If the key is a space key, it writes a newline character instead of "space". It also filters out any keys that contain "Key" since these are special keys like "Ctrl", "Alt", etc.
5. `on_release` Function: This function is called whenever a key is released. It checks if the pressed key is the Escape key (`Key.esc`). If it is, it returns `False`, which stops the listener and terminates the program.
6. Listener Setup and Execution: The script sets up a listener using `Listener` from `pynput.keyboard`, specifying the `on_press` and `on_release` functions. It then starts the listener using `listener.join()`, which starts listening for keyboard events.

This keylogger essentially records all keyboard input and saves it to a text file named "log.txt". It's a simple example that illustrates the basic concept of how keyloggers work and how they can be implemented using Python and libraries like `pynput`. 

## Project Structure:

```
Keylogger
|---- keylogger.py
|---- log.txt
```
