public class Persona {
    private double estatura; // En metros
    private double peso;     // En kilogramos

    // Constructor
    public Persona(double estatura, double peso) {
        this.estatura = estatura;
        this.peso = peso;
    }

    // Getters y setters para encapsulamiento
    public double getEstatura() {
        return estatura;
    }

    public void setEstatura(double estatura) {
        this.estatura = estatura;
    }

    public double getPeso() {
        return peso;
    }

    public void setPeso(double peso) {
        this.peso = peso;
    }

    // Método para calcular el IMC
    public double calcularIMC() {
        return peso / (estatura * estatura);
    }

    // Método para interpretar el IMC basado en categorías de la OMS
    public String interpretarIMC() {
        double imc = calcularIMC();
        if (imc < 18.5) {
            return "Bajo peso";
        } else if (imc < 24.9) { // Reducción de comparaciones
            return "Peso normal";
        } else if (imc < 29.9) {
            return "Sobrepeso";
        } else {
            return "Obesidad";
        }
    }
}
