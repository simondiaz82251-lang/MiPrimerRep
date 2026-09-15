taller1 = {"Ana", "Carlos", "Javier", "Lucía"}
taller2 = {"Lucía", "María", "Carlos", "Miguel"}
taller3 = {"Ana", "Javier", "José", "Miguel"}

# Unimos todos los estudiantes
todos = taller1 | taller2 | taller3

# Encontramos estudiantes que están en más de un taller
conflictos = (taller1 & taller2) | (taller2 & taller3) | (taller1 & taller3)

# Estudiantes que no tienen conflictos
sin_conflicto = todos - conflictos

# Mostrar resultados
print("ESTUDIANTES SIN CONFLICTOS:")
for estudiante in sorted(sin_conflicto):
    print("-", estudiante)

print("\nESTUDIANTES CON CONFLICTOS:")
for estudiante in sorted(conflictos):
    print("-", estudiante)
