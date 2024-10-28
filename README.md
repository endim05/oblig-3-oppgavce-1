# oblig-3-oppgavce-1

Oppgave a)
def my_max(lst):
    if len(lst) == 0:
        return None  # Return None if the list is empty
    max_value = lst[0]
    for num in lst:  # Iterate through the list and check if each element is greater than max_value
        if num > max_value:
            max_value = num
    return max_value  # Return the number with the highest value

def finn_storste(lst):
    max_value = my_max(lst)
    if max_value is None:
        return "Listen er tom."  # Return if the list is empty
    else:
        return f"Det største tallet i listen er {max_value}."  # Return the largest value in the list

resultat = finn_storste([1, 2, 3, 4, 5, 6])
print(resultat)  # Print the result

# Define the my_str_len function
def my_str_len(s):
    count = 0  # Keep track of how many characters are counted in the string
    for char in s:
        count += 1  # Increment count for each character
    return count

streng = "hei verden"
lengde = my_str_len(streng)
print(f"Strengen '{streng}' har {lengde} bokstaver.")  # Print the length of the string


oppgave b) Python

# Opprett klassen Student
class Student:
    def __init__(self, navn, student_id):
        self.navn = navn
        self.student_id = student_id

# Definer klassen for Gruppe - for å funksjonalisere forholdet mellom student og gruppe
class Gruppe:
    def __init__(self, gruppenavn, studenter):
        self.gruppenavn = gruppenavn
        self.studenter = studenter

# Funksjonen som finner ut hvilken gruppe en student hører til basert på student_id og gruppenr.
def finn_gruppe_for_student(student_id, grupper):
    for gruppe in grupper:
        for student in gruppe.studenter:
            if student.student_id == student_id:
                return gruppe.gruppenavn
    return "Studenten tilhører ingen gruppe"

# Eksempler som tar utgangspunkt i funksjonen
student1 = Student("Endi", 2004)
student2 = Student("Elion", 2001)
student3 = Student("Lars", 2005)
student4 = Student("Rexhep", 2003)

gruppe1 = Gruppe("Gruppe A", [student1, student2])
gruppe2 = Gruppe("Gruppe B", [student3, student4])

# Tilgjengelige grupper
grupper = [gruppe1, gruppe2]

print(finn_gruppe_for_student(2001, grupper))  # Output: Gruppe A
print(finn_gruppe_for_student(2003, grupper))  # Output: Gruppe B
print(finn_gruppe_for_student(1945, grupper))  # Output: Studenten tilhører ingen gruppe

oppgave b pyret

use context starter2024
# Opprett studenter
# student1 = Student ("Endi Muriqi, 1, gruppe1)
# student2 = Student ("Elion Olsen, 2, gruppe1)
# student3 = Student ("Lars Olsen, 3, gruppe2)
# student4 = Student ("Rexhep Isaksen, 4, gruppe2)
# student5 = Student ("Brage Salvesen, 5, gruppe1)

students = table:
    firstName, studentID, group
    row: "Endi Muriqi", "1", "Gruppe1"
    row: "Elion Olsen", "2", "Gruppe1"
    row: "Lars Olsen", "3", "Gruppe2"
    row: "Rexhep Isaksen", "4", "Gruppe2"
    row: "Brage Salvesen", "5", "Gruppe1"
end

fun finngruppe(navn, liste):
    liste.filter(lam(row): row["firstName"] == navn end)
end

# Test funksjonen
finngruppe("Endi Muriqi", students)


oppgave 3)

9.1.1

def moon_weight(earth_weight):
    """
    Compute weight on the moon from weight on Earth
    """
    return earth_weight * (1/6)

9.1.6.1

def num_to_str(numbers):
    return ["pos" if num > 0 else "neg" if num < 0 else "zero" for num in numbers]

numbers = [10, -5, 0]
result = num_to_str(numbers)
print(result)  # Output: ['pos', 'neg', 'zero']

def has_length_five(strings):
    return any(len(s) == 5 for s in strings)

strings = ["hello", "world", "Python", "AI"]
result = has_length_five(strings)
print(result)

def even_numbers_in_range(numbers):
    return [num for num in numbers if 10 <= num <= 20 and num % 2 == 0]

numbers = [5, 12, 15, 18, 21, 22]
result = even_numbers_in_range(numbers)
print(result)  # Output: [12, 18]


9.1.8.2
def all_z_words(words):
    return [word for word in words if 'z' in word]

def test_all_z_words():
    assert all_z_words([]) == []
    assert all_z_words(['buzz', 'fizz', 'dazzle']) == ['buzz', 'fizz', 'dazzle']

test_all_z_words()
print("All tests passed for first version!")

def all_z_words(words):
    """
    Return a list of words that start with the letter 'z' or 'Z'.
    """
    return list(filter(lambda w: w.startswith('z') or w.startswith('Z'), words))

words = ["zebra", "cow", "zoo", "cat"]
result = all_z_words(words)
print(result)

def test_zw_words():
    assert all_z_words(["zebra", "cow", "zoo", "cat"]) == ["zebra", "zoo"]

test_zwords()
print("all tests passed")

9.2.2

# Step 1: Create a dictionary that maps room names to the number of seats
rooms = {
    "Room A": 45,
    "Room B": 60,
    "Room C": 30,
    "Room D": 80,
    "Room E": 55
}

# Step 2.1: Look up how many seats are in a specific room
def get_seats(room_name):
    return rooms.get(room_name, "Room not found")

# Step 2.2: Change the capacity of a specific room to have 10 more seats
def add_seats(room_name):
    if room_name in rooms:
        rooms[room_name] += 10
        print(f"{room_name} now has {rooms[room_name]} seats.")







