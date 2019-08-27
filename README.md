# Aplicacion1
private void btnMostrarActionPerformed(java.awt.event.ActionEvent evt) {//GEN-FIRST:event_btnMostrarActionPerformed
        // Mostrar las propiedades del Objeto alumno   
        String codigo = alumno.getCodigo();
        String apellidos = alumno.getApellidos();
        String nombres = alumno.getNombres();
        int edad = alumno.getEdad();
        JOptionPane.showMessageDialog(rootPane, "Cogigo=" + codigo +
                "Apellidos=" + apellidos + " Nombres=" + nombres +
                "Edad=" + String.valueOf(edad));
    }//GEN-LAST:event_btnMostrarActionPerformed
    //Declar un objeto Alumno
    static Alumno alumno = new Alumno();
    private void btnRegistrarActionPerformed(java.awt.event.ActionEvent evt) {//GEN-FIRST:event_btnRegistrarActionPerformed
        /// Registrar los datos de un alumno
        String codigo = txtCodigo.getText().toString();
        String apellidos = txtApellidos.getText().toString();
        String nombres = txtNombres.getText().toString();
        int edad = Integer.parseInt(txtEdad.getText().toString());
        // Enviar datos al Objeto
        alumno.setCodigo(codigo);
        alumno.setApellidos(apellidos);
        alumno.setNombres(nombres);
        alumno.setEdad(edad);
        //Mnesaje de verificacion correcta
        JOptionPane.showMessageDialog(rootPane, "Se registro correctamente");
        // Limpiar las cajas de text
        txtCodigo.setText("");
        txtApellidos.setText("");
        txtNombres.setText("");
        txtEdad.setText("");
        // Enfocarnos en la caja de texto de Codigo
        txtCodigo.requestFocus();
    }//GEN-LAST:event_btnRegistrarActionPerformed

    private void btnEstudiarActionPerformed(java.awt.event.ActionEvent evt) {//GEN-FIRST:event_btnEstudiarActionPerformed
        // LLamar al metodo Estudiar del Objeto Alumno
        JOptionPane.showMessageDialog(rootPane, alumno.Estudiar());
