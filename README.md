TrabajoFinal
============
Controller

/mostrar {get};
	- trae un Icomentable;
		- toma los datos del Icomentable [en un Icomentable-form];
		- busca la lista de comentarios de ese Icomentable
		- manda el comentable-form y la lista de comentarios;

/agregar {post};
	- trae un comentario-form;
		- comentario-form > texto/aceptado/user/icomentable;
		- crea un comentario a partir de los datos de comentario-form;
		- carga el comentario a la DB;
		- vuelve al mostrar con el Icomentable

/eliminar {post};
	- trae un id del comentario
		- busca el comentario en la DB; } en un mismo metodo;
		- borra el comentario en la DB;	}
		- vuelve al mostrar con el Icomentable;

/editar {get};
	- trae un id del comentario
		- busca el comentario por id;
		- manda el comentario al jsp;

/editar {post};
	- trae el comentario-form:
		- pasa comentario-form a comentario;
		- pasa el comentario a un editar;

/blockear {get}
	- trae un id del comeentario
		- busca comentario en la DB; }
		- cambia el aceptado a false;}	en un mismo metodo;
		- guarda el comentario;	     } 


Mostrar {Icometnable} JSP

descripcion
	- nombre - nombre fabricante - precio

tabla [comentarios]
	- usuario - texto - /blokear{get} - /eliminar{get}

/agregar {post}
	-form
		- (hidden) usuario
		- (hidden) Icomentable
		- (hidden) aceptado
		- (text) texto
		[mandar]

Repositorio
	-/traer lista de comentarios;
	-/cargar comentarios a la BD;
	-/borrar comentario de la DB;
	-/editar el aceptado de false-true/true-false
