//Codigo Clases
public class Cliente {
    private String Nombre;
    private String Apellido;
    private String Cedula;
    private String Direccion;
   private String Telefono;

    public Cliente(String Nombre, String Apellido, String Cedula, String Direccion, String Telefono) {
        this.Nombre = Nombre;
        this.Apellido = Apellido;
        this.Cedula = Cedula;
        this.Direccion = Direccion;
        this.Telefono = Telefono;
    }

 public boolean validarCliente(){
    return  Nombre.matches("^[\\p{L}\\s]+$") 
            && Apellido.matches("^[\\p{L}\\s]+$") 
            && !Cedula.matches("\\d{10}") && Cedula.length()==10 
            && Direccion.matches("^[\\p{L}\\s]+$")
            && !Telefono.matches("\\d{10}") && Cedula.length()==10;
 }
}
