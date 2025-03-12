# Hoja-de-trabajo-5
Andy Cardona Paz. Carne: 1625125

"1."
def calcular_costo_agua(consumo, habitantes):
    if consumo < 15:
        tarifa = 5
    elif 15 <= consumo <= 30:
        if habitantes > 3:
            tarifa = 4
        elif habitantes == 3:
            tarifa = 4.5
        else:
            tarifa = 5
    else:  # consumo > 30
        if habitantes > 5:
            tarifa = 3.5
        elif habitantes % 2 == 0:
            tarifa = 4
        else:
            tarifa = 4.2

# Solicitar entrada al usuario
consumo = float(input("Ingrese el consumo en m³: "))
habitantes = int(input("Ingrese el número de habitantes: "))

# Calcular y mostrar el costo del agua
costo = calcular_costo_agua(consumo, habitantes)
print(f"El costo total del consumo de agua es: Q{costo:.2f}")

"2."
def restriccion_circulacion(ano_vehiculo, placa):
    import datetime

    
    ano_actual = datetime.datetime.now().year

   
    if ano_actual - ano_vehiculo > 25:
        print("Advertencia: Mantenimiento obligatorio para vehículos con más de 25 años de antigüedad.")

   
    if ano_vehiculo >= 2001:
        ultimo_digito = int(placa[-1])

        if ultimo_digito in [0, 2, 4, 6, 8]:
            print("No circula los lunes.")
        elif ultimo_digito in [1, 3, 5, 7, 9]:
            print("No circula los viernes.")

      
        if ano_vehiculo % 2 == 0:
            print("Restricción adicional: Los sábados solo circula hasta el mediodía.")


ano_vehiculo = int(input("Ingrese el año del vehículo: "))
placa = input("Ingrese el número de placa: ")


restriccion_circulacion(ano_vehiculo, placa)
