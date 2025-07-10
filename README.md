# constructores-java-
/**
 * Clase Empleado con varios constructores para demostrar sobrecarga
 */
public class Empleado {
    private String nombre;
    private int id;
    private double salario;

    // Constructor por defecto
    public Empleado() {
        this.nombre = "Desconocido";
        this.id = 0;
        this.salario = 0.0;
    }

    // Constructor parametrizado con nombre
    public Empleado(String nombre) {
        this(nombre, 0, 0.0); // cadena de constructores
    }

    // Constructor parametrizado con nombre e id
    public Empleado(String nombre, int id) {
        this(nombre, id, 0.0);
    }

    // Constructor parametrizado completo
    public Empleado(String nombre, int id, double salario) {
        this.nombre = nombre;
        this.id = id;
        this.salario = salario;
    }

    // Constructor copia
    public Empleado(Empleado otro) {
        this.nombre = otro.nombre;
        this.id = otro.id;
        this.salario = otro.salario;
    }

    // Método para mostrar datos
    public void mostrarInfo() {
        System.out.println("Nombre: " + nombre + ", ID: " + id + ", Salario: " + salario);
    }
}
public class Main {
    public static void main(String[] args) {
        Empleado e1 = new Empleado();
        Empleado e2 = new Empleado("Ana");
        Empleado e3 = new Empleado("Luis", 123);
        Empleado e4 = new Empleado("María", 456, 55000.0);
        Empleado e5 = new Empleado(e4); // copia

        e1.mostrarInfo();
        e2.mostrarInfo();
        e3.mostrarInfo();
        e4.mostrarInfo();
        e5.mostrarInfo();
    }
}
