Reto: Describe qué cambios observas o qué sucedió en comparación con la versión anterior de tu aplicación.

Primero, Inyección Incorrecta de Servicios Scoped en un Singleton: Al intentar crear una instancia de MangaService como Singleton, también se deben crear sus dependencias. Sin embargo, si estas dependencias están registradas con un ciclo de vida Scoped, no pueden mantenerse activas durante toda la vida de la aplicación, lo que provoca un error.

Conflictos y Duplicación en la Inyección de Dependencias: Has registrado MangaService múltiples veces con diferentes ciclos de vida (Scoped, Transient, Singleton), lo cual causa conflictos. En versiones anteriores, este problema no se presentaba porque los servicios solo se registraban una vez con un ciclo de vida específico.

Además, se ha agregado una nueva librería al proyecto que maneja registros de mangas para verificar el correcto funcionamiento de la API.

