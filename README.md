public class Persona {
    private double estatura; // En metros
    private double peso;     // En kilogramos

   
    public Persona(double estatura, double peso) {
        this.estatura = estatura;
        this.peso = peso;
    }

    
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

    
    public double calcularIMC() {
        return peso / (estatura * estatura);
    }

   
    public String interpretarIMC() {
        double imc = calcularIMC();
        if (imc < 18.5) {
            return "Bajo peso";
        } else if (imc < 24.9) {
            return "Peso normal";
        } else if (imc < 29.9) {
            return "Sobrepeso";
        } else {
            return "Obesidad";
        }
    }
}
