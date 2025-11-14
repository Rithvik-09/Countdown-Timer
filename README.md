# Countdown-Timer
This mini-project is written in Python. It takes an input in minutes, converts the minutes into seconds, and performs a countdown until it reaches zero.
import time

def timer(seconds):
    while seconds:
        mins, secs = divmod(seconds, 60)
        timer = '{:02d}:{:02d}'.format(mins, secs)
        print(timer, end="\r")
        time.sleep(1)
        seconds -= 1
    print("Time's up!")
if __name__ == "__main__":
    try:
        total_seconds = int(input("Enter the time in seconds: "))
        timer(total_seconds)
    except ValueError:
        print("Please enter a valid number of seconds.")
