# Help-Martians
Homework for Mr Tauheed
def find_cargo():
    # Initialize arrays to store information about each box
    marks = [0, 0, 0]  # Kilometer marks
    weights = [0, 0, 0]  # Weights of the boxes

    while True:
        # Input kilometer marks for each box
        for i in range(3):
            marks[i] = int(input(f"Enter the kilometer mark for box {i + 1}: "))

        # Simulate the movement of boxes with legs
        for i in range(3):
            weights[i] = int(input(f"Enter the weight buried at kilometer {marks[i]}: "))
            marks[i] = (marks[i] + weights[i]) % 7  # Move the box if necessary

        # Check if the total weight is 713
        if sum(weights) == 713:
            print("Congratulations! You found all the boxes.")
            break
        else:
            print("The total weight is not 713. Try again.")

# Call the function to start the program
find_cargo()
