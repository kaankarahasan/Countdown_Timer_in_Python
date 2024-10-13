# Countdown_Timer_in_Python

This Python program counts down from a user-defined time and displays a "TIME'S UP!" message once the countdown reaches zero.

## Usage

This program utilizes Python's `time` module to create a simple countdown timer that can be run from the terminal.

### Requirements

- Python 3.x must be installed.

### How to Run?

1. Navigate to the directory where your `countdown.py` file is located, and run the following command:
    ```bash
    python countdown.py
    ```

2. Once the program starts, you'll be prompted to enter a time in seconds (e.g., 120 seconds). The program will then start the countdown.

### Code Explanation

The `countdown.py` file follows these steps:
- It prompts the user to enter a time in seconds for the countdown.
- As the countdown proceeds, the remaining time is displayed in the format `HH.MM.SS` (hours, minutes, and seconds).
- The display updates every second.
- When the countdown reaches zero, the message "TIME'S UP!" is printed on the screen.

```python
import time

my_time = int(input("Enter the time in seconds: "))

for x in range(my_time, 0, -1):
    seconds = x % 60
    minutes = int(x / 60) % 60
    hours = int(x / 3600)
    print(f"{hours:02}.{minutes:02}.{seconds:02}")
    time.sleep(1)

print("TIME'S UP!")
