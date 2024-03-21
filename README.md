# CIS129_YourName_Lab5
 # Lab 5 The Bottle Return Program
# Author: [Nghia Tran]
# Date: [03/20/2024]
# Description: This program keeps track of the total number of bottles collected for seven days and calculates the total payout.

def main():
    # Step 1: Declare variables below 
    total_bottles = 0
    counter = 1
    today_bottles = 0
    total_payout = 0
    keep_going = 'y'
	
    # Step 2: Loop to run program again
    while keep_going == 'y':
        # Step 3: Code to set value of variables
        total_bottles = get_bottles()
        total_payout = calc_payout(total_bottles)
        print_info(total_bottles, total_payout)
        
        keep_going = input("Do you want to enter another week's worth of data? (Enter y or n): ")

# Function to get number of bottles for each day
def get_bottles():
    NBR_OF_DAYS = 7
    total_bottles = 0
    counter = 0

    while counter < NBR_OF_DAYS:
        today_bottles = int(input(f"Enter number of bottles returned for day #{counter + 1}: "))
        total_bottles += today_bottles
        counter += 1
    
    return total_bottles

# Function to calculate the payout
def calc_payout(total_bottles):
    PAYOUT_PER_BOTTLE = 0.10
    total_payout = total_bottles * PAYOUT_PER_BOTTLE
    return total_payout

# Function to print total bottles and total payout
def print_info(total_bottles, total_payout):
    print("\nThe total number of bottles collected is", total_bottles)
    print("The total paid out is $", total_payout)

if __name__ == "__main__":
    main()
