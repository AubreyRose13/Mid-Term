Week 1 script projects

myinfo.py
print(“Name: Aubrey Price”) 
print(“Address: 1229 West 5th Street Okmulgee OK, 74447”)
print(“Telephone: 918 758 7913”)

rectangle.py
length = float(input("Enter the length: "))
width = float(input("Enter the width: "))
area = length * width
print("The area is", area, "square untis.")

triangle.py
base = float(input("Enter the base: "))
height = float(input("Enter the height: "))
area = .5 * base * height
print("The area is", area, "square untis.")

circle.py
radius = float(input("Enter the radius: "))
area = 3.14 * radius **2
print("The area is", area, "square untis.")

cuboid.py
height = float(input("Enter the height: "))
width = float(input("Enter the width: "))
depth = float(input("Enter the depth: "))
area = height * width * depth * 2
print("The area is", area, "square untis.")

Week 2 Script Projects

cube.py
cubeEdge = int(input("Enter the cube's edge: "))
cubeArea = int(input("Enter the cube's area: "))
cubeArea = (6)cubeEdge * 2
print("The surface area is " + str(cubeArea) + " square units.")

momentum.py
Mass = float(input("Mass : "))
Velocity =float(input("Velocity : "))
print("")
Momentum = Mass * Velocity
print("The object's momentum is " + str(Momentum))
4 / 9

Week 3 Script Projects

employeepay.py
hourly_wage = float(input("Enter hourly wage: "))
regular_hours = float(input("Enter total regular hours: "))
overtime_hours = float(input("Enter total overtime hours: "))

overtime_pay = overtime_hours * 1.5 * hourly_wage
total_weekly_pay = hourly_wage * regular_hours + overtime_pay

print("Total weekly pay: $" + str(total_weekly_pay))

minutes.py
def calculate_minutes(years):
minutes_per_hour = 60
hours_per_day = 24
days_per_year = 365
years * days_per_year * hours_per_day * minutes_per_hour

years = int(input("Enter the number of years: "))

calculate_minutes(years)
print(f"There are {minutes} minutes in {years} years.")

taxform.py
TAX_RATE = 0.20
STANDARD_DEDUCTION = 10000.0
DEPENDENT_DEDUCTION = 3000.0
# Request the inputs
grossIncome = float(input("Enter the gross income: 12345.67 "))
numDependents = int(input("Enter the number of dependents: 1"))
# Compute the income tax
taxableIncome = grossIncome - STANDARD_DEDUCTION - \
DEPENDENT_DEDUCTION * numDependents
incomeTax = taxableIncome * TAX_RATE
# Display the income tax
print("The income tax is $" + str(round(incomeTax,2)))

Week 4 Script Projects

bouncy.py
def calculate_total_distance(initial_height, bounciness_index, num_bounces):
    total_distance = initial_height 

    current_height = initial_height
    for _ in range(num_bounces):
        current_height *= bounciness_index  
        total_distance += 2 * current_height  

    return total_distance

def main():
    try:
        initial_height = float(input("Enter the initial height from which the ball is dropped (in feet): "))
        bounciness_index = float(input("Enter the bounciness index (between 0 and 1): "))
        num_bounces = int(input("Enter the number of bounces: "))
        
        if bounciness_index < 0 or bounciness_index > 1:
            print("Bounciness index must be between 0 and 1.")
            return

    except ValueError:
        print("Invalid input! Please enter numerical values.")
        return

    total_distance = calculate_total_distance(initial_height, bounciness_index, num_bounces)
    print(f"The total distance traveled by the ball after {num_bounces} bounce(s) is {total_distance:.2f} feet.")

if __name__ == "__main__":
    main()

count.py
for count in range(4):
    print(count, end = "")

countdown.py
number = 2
exponent = 3
product = 1
for eachPass in range(exponent):
product = product * number
print(product, end = " ")

data.py
print(list(range(4)))
print(list(range(1, 5)))
for number in {6, 4, 8}:
print(number, end=" ")

equilateral.py
def is_equilateral(a, b, c):
    return a == b == c

def main():
    print("Enter the lengths of the three sides of a triangle:")
    
try:
    a = float(input("Length of side a: "))
    b = float(input("Length of side b: "))
    c = float(input("Length of side c: "))
except ValueError:
    print("Invalid input! Please enter numerical values.")

if is_equilateral(a, b, c):
    print("The triangle is an equilateral triangle.")
else:
    print("The triangle is not an equilateral triangle.")

if __name__ == "__main__":
    main()

exponet.py
number = 2
exponent = 3
product = 1
for eachPass in range(exponent):
product = product * number
print(product, end = " ")

format.py
for exponent in range(7, 11):
    print(f"[{exponent} {10 ** exponent}]")
[7 10000000]
[8 100000000]
[9 1000000000]
[10 10000000000]

population.py
def calculate_population(initial_population, growth_rate, growth_time, total_time):
    num_growth_periods = total_time // growth_time
    
    final_population = initial_population * (growth_rate ** num_growth_periods)
    
    return final_population

def main():
    try:
        initial_population = int(input("Enter the initial number of organisms: "))
        growth_rate = float(input("Enter the growth rate (a real number greater than 0): "))
        growth_time = float(input("Enter the time (in hours) to achieve this growth rate: "))
        total_time = float(input("Enter the total time (in hours) for population growth: "))
        
        if initial_population <= 0 or growth_rate <= 0 or growth_time <= 0 or total_time <= 0:
            print("All input values must be greater than 0.")
            return

    except ValueError:
        print("Invalid input! Please enter numerical values.")
        return

    final_population = calculate_population(initial_population, growth_rate, growth_time, total_time)
    
    print(f"The predicted total population after {total_time} hours is: {final_population}")

if __name__ == "__main__":
    main()

range.py
product = 1
for count in range(4):
product = product * (count + 1)
product
product = 1
for count in range(1,5):
product = product * count
product
list(range(1, 6, 1))
[1, 2, 3, 4, 5]
list(range(1, 6, 2))
[1, 3, 5]
list(range(1, 6, 3))
[1, 4]

sum.py
theSum = 0 
for count in range(2, 11, 2):
theSum += count
theSum
30

summation.py
lower = int(input("Enter the lower bound: "))
upper = int(input("Enter the upper bound: "))
theSum = 0 
for number in range(lower, upper + 1):
theSum = theSum + number
theSum

Week 5 Script Projects

guess.py
lower = int(input("Enter the lower bound: "))
upper = int(input("Enter the upper bound: "))
theSum = 0 
for number in range(lower, upper + 1):
theSum = theSum + number
theSum

salary.py
def main():
    # Get user inputs
    starting_salary = float(input("Enter the starting salary: "))
    percentage_increase = float(input("Enter the percentage increase (e.g., for 2%, enter 2): "))
    number_of_years = int(input("Enter the number of years in the schedule: "))

    # Calculate the actual increase factor
    increase_factor = 1 + (percentage_increase / 100)

    # Print the header for the salary schedule
    print(f"\n{'Year':<10}{'Salary':<10}")
    print("-" * 20)

    # Initialize the salary for the first year
    salary = starting_salary

    # Generate the salary schedule
    for year in range(1, number_of_years + 1):
        print(f"{year:<10}{salary:<10.2f}")
        salary *= increase_factor  # Update the salary for the next year

if __name__ == "__main__":
    main()

tidbit.py
def main():
    # Get user inputs
    starting_salary = float(input("Enter the starting salary: "))
    percentage_increase = float(input("Enter the percentage increase (e.g., for 2%, enter 2): "))
    number_of_years = int(input("Enter the number of years in the schedule: "))

    # Calculate the actual increase factor
    increase_factor = 1 + (percentage_increase / 100)

    # Print the header for the salary schedule
    print(f"\n{'Year':<10}{'Salary':<10}")
    print("-" * 20)

    # Initialize the salary for the first year
    salary = starting_salary

    # Generate the salary schedule
    for year in range(1, number_of_years + 1):
        print(f"{year:<10}{salary:<10.2f}")
        salary *= increase_factor  # Update the salary for the next year

if __name__ == "__main__":
    main()

Week 6 Script Projects

copyfile.py
def main():
    # Get user inputs
    starting_salary = float(input("Enter the starting salary: "))
    percentage_increase = float(input("Enter the percentage increase (e.g., for 2%, enter 2): "))
    number_of_years = int(input("Enter the number of years in the schedule: "))

    # Calculate the actual increase factor
    increase_factor = 1 + (percentage_increase / 100)

    # Print the header for the salary schedule
    print(f"\n{'Year':<10}{'Salary':<10}")
    print("-" * 20)

    # Initialize the salary for the first year
    salary = starting_salary

    # Generate the salary schedule
    for year in range(1, number_of_years + 1):
        print(f"{year:<10}{salary:<10.2f}")
        salary *= increase_factor  # Update the salary for the next year

if __name__ == "__main__":
    main()

decrypt.py
def main():
    # Get user inputs
    starting_salary = float(input("Enter the starting salary: "))
    percentage_increase = float(input("Enter the percentage increase (e.g., for 2%, enter 2): "))
    number_of_years = int(input("Enter the number of years in the schedule: "))

    # Calculate the actual increase factor
    increase_factor = 1 + (percentage_increase / 100)

    # Print the header for the salary schedule
    print(f"\n{'Year':<10}{'Salary':<10}")
    print("-" * 20)

    # Initialize the salary for the first year
    salary = starting_salary

    # Generate the salary schedule
    for year in range(1, number_of_years + 1):
        print(f"{year:<10}{salary:<10.2f}")
        salary *= increase_factor  # Update the salary for the next year

if __name__ == "__main__":
    main()

encrypt.py
def main():
    # Get user inputs
    starting_salary = float(input("Enter the starting salary: "))
    percentage_increase = float(input("Enter the percentage increase (e.g., for 2%, enter 2): "))
    number_of_years = int(input("Enter the number of years in the schedule: "))

    # Calculate the actual increase factor
    increase_factor = 1 + (percentage_increase / 100)

    # Print the header for the salary schedule
    print(f"\n{'Year':<10}{'Salary':<10}")
    print("-" * 20)

    # Initialize the salary for the first year
    salary = starting_salary

    # Generate the salary schedule
    for year in range(1, number_of_years + 1):
        print(f"{year:<10}{salary:<10.2f}")
        salary *= increase_factor  # Update the salary for the next year

if __name__ == "__main__":
    main()

Week 7 Script Projects

navigate.py
# navigate.py

def main():
    # Prompt user for a filename
    filename = input("Enter the filename: ")
    
    try:
        # Read the lines from the file into a list
        with open(filename, 'r') as file:
            lines = file.readlines()
        
        while True:
            # Print the number of lines in the file
            print(f"Number of lines in the file: {len(lines)}")
            
            # Prompt user for a line number
            line_number = int(input("Enter a line number (0 to quit): "))
            
            if line_number == 0:
                print("Exiting the program.")
                break
            
            # Check if the line number is valid
            if 1 <= line_number <= len(lines):
                print(f"Line {line_number}: {lines[line_number - 1].strip()}")
            else:
                print("Invalid line number. Please try again.")

    except FileNotFoundError:
        print("File not found. Please check the filename and try again.")
    except ValueError:
        print("Please enter a valid integer for the line number.")

if __name__ == "__main__":
    main()

stats.py
# stats.py

def mean(numbers):
    """Computes the average of a list of numbers."""
    if not numbers:
        return 0
    return sum(numbers) / len(numbers)

def median(numbers):
    """Computes the median of a list of numbers."""
    if not numbers:
        return 0
    sorted_numbers = sorted(numbers)
    n = len(sorted_numbers)
    mid = n // 2
    if n % 2 == 0:
        return (sorted_numbers[mid - 1] + sorted_numbers[mid]) / 2
    else:
        return sorted_numbers[mid]

def mode(numbers):
    """Computes the mode of a list of numbers."""
    if not numbers:
        return 0
    frequency = {}
    for number in numbers:
        frequency[number] = frequency.get(number, 0) + 1

    max_count = max(frequency.values())
    modes = [key for key, count in frequency.items() if count == max_count]

    if len(modes) == len(frequency):
        return 0  # All values occur with the same frequency
    return modes[0]  # Return the first mode

def main():
    """Tests the mean, median, and mode functions."""
    test_data = [1, 2, 2, 3, 4, 5, 5, 5, 6]
    print("Test data:", test_data)
    print("Mean:", mean(test_data))
    print("Median:", median(test_data))
    print("Mode:", mode(test_data))

if __name__ == "__main__":
    main()
    
