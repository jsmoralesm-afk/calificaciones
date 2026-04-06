def promedio(notas):
    suma_total = 0
    for nota in notas:
        suma_total += nota
    return suma_total / len(notas)


def mayor(notas):
    mayor_nota = notas[0]
    for nota in notas:
        if nota > mayor_nota:
            mayor_nota = nota
    return mayor_nota


def menor(notas):
    menor_nota = notas[0]
    for nota in notas:
        if nota < menor_nota:
            menor_nota = nota
    return menor_nota


def contar_aprobados(notas, minimo=61):
    contador = 0
    for nota in notas:
        if nota >= minimo:
            contador += 1
    return contador


def reporte(notas):
    print("REPORTE DE NOTAS")
    print("-------------------")
    print("Promedio:", round(promedio(notas), 2))
    print("Nota más alta:", mayor(notas))
    print("Nota más baja:", menor(notas))
    print("Aprobados:", contar_aprobados(notas))
    print("Reprobados:", len(notas) - contar_aprobados(notas))


def histograma(notas):
    print("\nHISTOGRAMA")
    print("-------------")
    for nota in notas:
        cantidad_estrellas = nota // 5
        print(str(nota) + ": " + "*" * cantidad_estrellas)


# PRUEBA (esto es MUY importante)
notas = [85, 42, 73, 61, 55, 90, 38, 77, 95, 60]

reporte(notas)
histograma(notas)
