def binary_to_decimal(binary):
    decimal = 0
    power = len(binary) - 1
    for digit in binary:
        decimal += int(digit) * (2 ** power)
        power -= 1
    return decimal
def decimal_to_hexadecimal(decimal):
    hexadecimal = ""
    while decimal > 0:
        remainder = decimal % 16
        if remainder < 10:
            hexadecimal = str(remainder) + hexadecimal
        else:
            hexadecimal = chr(ord('A') + remainder - 10) + hexadecimal
        decimal //= 16
    return hexadecimal

def decimal_to_octal(decimal):
    octal = ""
    while decimal > 0:
        remainder = decimal % 8
        octal = str(remainder) + octal
        decimal //= 8
    return octal

print(f"Nama : Muhammad Rizqi")
print(f"NPM : 07352211146")
binary_number = input("Masukkan bilangan biner: ")
decimal_number = binary_to_decimal(binary_number)
octal_number = decimal_to_octal(decimal_number)
hexadecimal_number = decimal_to_hexadecimal(decimal_number)


print("Hasil konversi ke desimal:", decimal_number)
print("Hasil konversi ke oktal:", octal_number)
print("Hasil konversi ke heksadesimal:", hexadecimal_number)
