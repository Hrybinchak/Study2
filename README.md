# Study2
class Driver:
    def __init__(self, name):
        self.name = name
        self.trips = []

    def add_trip(self, loading_point, distance):
        self.trips.append((loading_point, distance))

    def calculate_salary(self, rate):
        total_distance = sum(distance for _, distance in self.trips)
        salary = total_distance * rate
        return salary


# Example usage:
drivers = []

# Create drivers
driver1 = Driver("John")
driver2 = Driver("Alice")

# Add trips for driver1
driver1.add_trip("Loading Point 1", 50)
driver1.add_trip("Loading Point 2", 30)
driver1.add_trip("Loading Point 3", 20)

# Add trips for driver2
driver2.add_trip("Loading Point 4", 40)
driver2.add_trip("Loading Point 5", 25)
driver2.add_trip("Loading Point 6", 35)

# Add drivers to the list
drivers.append(driver1)
drivers.append(driver2)

# Calculate and display salaries
for driver in drivers:
    salary = driver.calculate_salary(0.6)
    print(f"Driver: {driver.name}")
    print(f"Total Distance: {sum(distance for _, distance in driver.trips)} km")
    print(f"Salary: ${salary}\n")
