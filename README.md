# Prueba

Primer paso crear el proyecto, en este caso use la tecnologia de Java + sql.

creando el programa lo cree en formato "Java With Ant" con el projects "jAVA Applicaction",
Una vez creado el proyecto realice 1 clase llamada ConexionSql, y 3 clases JFrame.

En la clase Conexion realice lo siguientes pasos: 

1- Importar las librerias necesarias para poder realizar el programas: 
              import java.sql.*;
              import java.util.logging.Level;
              import java.util.logging.Logger;
              import javax.swing.JOptionPane;

2- Realizar la conexion a la base de datos: 
hice una clases static para poder llamarla en los demas Jframe class, 

public static Connection obtenerconexion(){
    String url = "jbdc:sqlserver://localhost:1433;"
            + "database=proyecto;"
            + "user=UseJAva;"
            + "password=12345;";
            //Me concete a la base de datos con esta formula simple.
        try {
            Connection con;
            con = DriverManager.getConnection(url);
            return con;
        } catch (SQLException ex) {
            System.out.println(ex.toString());
            return null;
        }
        /* El try catch es para verificar que se encuentre el usuario y contrasena
           del usuario
        */
    }
    
3- Crear la clase inicio que es donde esta el login del proyecto.
    Importe lo siguiente: 
    import java.sql.*;
    import java.util.logging.Level;
    import java.util.logging.Logger;
aplique algunas formulas para poder verificar que si el usuario es temporal o visitante te lleve a su respectiva ventana
y una operaciones para saber si las contrasenas existen junto con el usuario en la base de dato.

4- Cree 2 JFrame para que te muestre un mensaje depediendo de tu usuario de login te llevara a la ventana respectiva.

Use sql server 2019 y neatbeans 14.0
