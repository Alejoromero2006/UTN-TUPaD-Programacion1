UTN-TUPaD-Programacion1

C:\\Users\\alejo\\AppData\\Local\\Temp\\18aceee0-3018-4256-99ee-e4ad92cdde0b\_TP INTEGRADOR REPETITIVAS-CONDICIONALES-SECUENCIALES (1).zip.e0b\\TP INTEGRADOR REPETITIVAS-CONDICIONALES-SECUENCIALES.py
===







\#Actividad 1:

\# 1. Pedir nombre del cliente - solo letras

nombre = input("Cliente: ")

while not nombre.isalpha():

&#x20;   print("Error: El nombre solo debe contener letras y no estar vacío.")

&#x20;   nombre = input("Cliente: ")



\# 2. Pedir cantidad de productos - entero positivo

cantidad = input("Cantidad de productos: ")

while not cantidad.isdigit() or int(cantidad) == 0:

&#x20;   print("Error: Ingresá un número entero mayor a 0.")

&#x20;   cantidad = input("Cantidad de productos: ")

cantidad = int(cantidad)



total\_sin\_descuento = 0

total\_con\_descuento = 0



\# 3. Por cada producto

for i in range(1, cantidad + 1):

&#x20;   # Pedir precio - entero

&#x20;   precio = input(f"Producto {i} - Precio: ")

&#x20;   while not precio.isdigit():

&#x20;       print("Error: El precio debe ser un número entero.")

&#x20;       precio = input(f"Producto {i} - Precio: ")

&#x20;   precio = int(precio)

&#x20;   

&#x20;   # Pedir descuento S/N

&#x20;   descuento = input(f"Producto {i} - Descuento (S/N): ")

&#x20;   while descuento.lower() != 's' and descuento.lower() != 'n':

&#x20;       print("Error: Ingresá S o N.")

&#x20;       descuento = input(f"Producto {i} - Descuento (S/N): ")

&#x20;   

&#x20;   total\_sin\_descuento += precio

&#x20;   

&#x20;   # Aplicar 10% si tiene descuento

&#x20;   if descuento.lower() == 's':

&#x20;       precio\_con\_descuento = precio \* 0.9

&#x20;       total\_con\_descuento += precio\_con\_descuento

&#x20;   else:

&#x20;       total\_con\_descuento += precio





ahorro = total\_sin\_descuento - total\_con\_descuento

promedio = total\_con\_descuento / cantidad





print(f"Total sin descuentos: ${total\_sin\_descuento}")

print(f"Total con descuentos: ${total\_con\_descuento:.2f}")

print(f"Ahorro: ${ahorro:.2f}")

print(f"Promedio por producto: ${promedio:.2f}")



