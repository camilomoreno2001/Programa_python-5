# Programa_python-5
programacion problema 5 
# ==================================================================================
# CURSO: FUNDAMENTOS DE PROGRAMACIÓN
# FASE 5: EVALUACIÓN FINAL POA
# ESTUDIANTE: CRISTIAN CAMILO MORENO GÓMEZ
# PROBLEMA SELECCIONADO: PROBLEMA 5 – CONTROL DE HORAS LABORALES
# ==================================================================================

# MATRIZ DE DATOS
# [Nombre, Lunes, Martes, Miércoles, Jueves, Viernes]

recursos = [
    ["Carlos", 8, 8, 9, 8, 10],
    ["María", 7, 8, 8, 7, 8],
    ["Juan", 10, 9, 8, 9, 10],
    ["Luisa", 6, 7, 8, 7, 6]
]

UMBRAL_HORAS = 40

# FUNCIÓN PARA CALCULAR HORAS Y CLASIFICACIÓN

def calcular_jornada(datos_recurso):

    nombre = datos_recurso[0]

    total_horas = sum(datos_recurso[1:])

    if total_horas > UMBRAL_HORAS:
        clasificacion = "Sobretiempo"
    else:
        clasificacion = "Horario Estándar"

    return nombre, total_horas, clasificacion


# PROGRAMA PRINCIPAL

def main():

    print("=== REPORTE DE HORAS SEMANALES ===")

    for recurso in recursos:

        nombre, total, jornada = calcular_jornada(recurso)

        print("\n-----------------------------")
        print("Nombre:", nombre)
        print("Total semanal:", total)
        print("Clasificación:", jornada)

if __name__ == "__main__":
    main()
