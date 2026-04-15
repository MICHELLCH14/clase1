# clase1
class Estudiante:
    """
    Clase estudiante que permite crear objetos de tipo estudiante.
    """

    def __init__(self, nombre, cedula, semestre, email):
        self.__nombre = nombre
        self.__cedula = cedula
        self.__semestre = semestre
        self.__email = email

    # GETTERS
    @property
    def nombre(self):
        return self.__nombre

    @property
    def cedula(self):
        return self.__cedula

    @property
    def semestre(self):
        return self.__semestre

    @property
    def email(self):
        return self.__email

    # SETTERS
    @nombre.setter
    def nombre(self, nuevo_nombre):
        self.__nombre = nuevo_nombre

    @cedula.setter
    def cedula(self, nueva_cedula):
        self.__cedula = nueva_cedula

    @semestre.setter
    def semestre(self, nuevo_semestre):
        self.__semestre = nuevo_semestre

    @email.setter
    def email(self, nuevo_email):
        self.__email = nuevo_email

    def __str__(self):
        return f'Estudiante [nombre: {self.__nombre}, cedula: {self.__cedula}, semestre: {self.__semestre}, email: {self.__email}]'


# PRUEBA
if __name__ == '__main__':
    estudiante1 = Estudiante('michelle', '1234567890', '4er semestre', 'michelle.cccc@example.com')

    print(estudiante1)

    print(f"Nombre: {estudiante1.nombre}")
    print(f"Cédula: {estudiante1.cedula}")
    print(f"Semestre: {estudiante1.semestre}")
    print(f"Email: {estudiante1.email}")

    estudiante1.email = 'michelle.cccc@gmail.com'
    print(f"Nuevo Email: {estudiante1.email}")
    print(estudiante1)
