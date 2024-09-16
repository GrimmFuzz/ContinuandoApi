# ContinuandoApi
Desafío: Explica los cambios que identificas o lo que ocurrió en relación con la versión anterior de tu aplicación.

Uno de los problemas que surgieron es una inyección incorrecta de dependencias Scoped dentro de un Singleton. Al intentar crear el servicio MangaService como Singleton, se requiere también instanciar sus dependencias. Si alguna de estas está configurada como Scoped, no durará todo el ciclo de vida de la aplicación, lo que genera un fallo.

Otro problema es la duplicación y conflicto en la inyección de dependencias, ya que MangaService fue registrado varias veces con diferentes configuraciones de ciclo de vida (Scoped, Transient, Singleton). En las versiones anteriores esto no ocurría porque los servicios solo se registraban una vez y de forma consistente.

Además, se incorporó una librería que almacena datos de mangas para comprobar si la API sigue funcionando correctamente.
