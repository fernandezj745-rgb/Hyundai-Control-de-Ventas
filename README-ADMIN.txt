HYUNDAI CONTROL DE VENTAS - MODELO DE PERMISOS

Administrador principal: fernandezj745@gmail.com
Usuarios de equipo autorizados:
- thebotssense@gmail.com
- tvcuetoandres@gmail.com

Nueva estructura Firestore:
- sales/{saleId}: una venta por documento, con ownerUid y ambassadorEmail.
- settings/goals: metas compartidas; solo el administrador puede escribir.
- profiles/{uid}: nombre del embajador asociado a su cuenta.

Permisos:
- Los tres usuarios pueden leer las ventas y registrar ventas propias.
- Un embajador solo puede borrar ventas cuyo ownerUid coincide con su UID.
- El administrador puede borrar cualquier venta y modificar metas.
- El administrador puede actualizar/eliminar cualquier perfil.

IMPORTANTE SOBRE EL REINICIO:
La aplicación nueva deja de leer y escribir shared/main. Los datos antiguos de shared/main no se importan a la nueva estructura, pero este paquete NO borra físicamente ese documento. Se conserva en Firebase como respaldo residual hasta que el administrador decida eliminarlo manualmente después de verificar la nueva aplicación.

PUBLICACIÓN:
Desde la raíz del proyecto:
  firebase deploy --only firestore:rules,hosting --project seguimiento-de-ventas-1f818

No se ha realizado una prueba real contra el proyecto Firebase ni con los tres usuarios. Tras desplegar, verificar primero inicio de sesión, alta de venta en cada cuenta, visibilidad en los otros dispositivos, borrado propio y bloqueo de borrado ajeno.
