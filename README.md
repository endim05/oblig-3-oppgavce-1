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






