# operacionesconfunciones.py
envio link de codigo de operaciones (suma,resta,multiplicacion y division) utilizando funcion sucesora y antecesora 



def S(n):
    return n + 1

def A(n):
    return n - 1 if n > 0 else 0

def suma(a, b):
    return a if b == 0 else suma(S(a), A(b))

def multiplicacion(a, b):
    return 0 if b == 0 else suma(a, multiplicacion(a, A(b)))

def resta(a, b):
    return a if b == 0 else resta(A(a), A(b))

def division(a, b):
    if b == 0:
        raise ValueError("No se puede dividir por cero")
    return 0 if a < b else S(division(resta(a, b), b))
