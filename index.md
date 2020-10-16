# Bienvenido

# Git y GitHub 

## ¿Qué es Git?

Git es un sistema de control de versiones en forma local; Git es muy útil debido a su simpleza y su gran potencial; la pregunta  
que todos nos hacemos es ¿para qué me sirve usar Git? Y la respuesta es aún mejor; Git es tu salvador ya que con él podrás controlar  
cada detalle y cada versión de cualquier cosa que hagas; ya sean programas, documentos, presentaciones, cualquier cosa  a la que te  
dediques. Git NO es lo mismo que GitHub NO debes confundirlos.

## ¿Qué es GitHub?

Si git es un sistema de control de versiones, GitHub es tu bodega para guardar TODOS los cambios de tu desarrollo; la ventaja de github  
es que es en línea y que muchas personas pueden acceder a tu ''almacén'' para poder visualizar tus cambios, versiones, etc. 

>Github es indispensable en un ambiente de desarrollo

## ¿Que ventajas tiene usar estas dos herramientas?

No voy a confundirte más, te voy a poner un ejemplo práctico: supongamos que el día de hoy el gerente solicita un sistema y lo terminas en una semana;  
le vas presentando los cambios (sin guardar) al gerente y al final de la semana él los aprueba y tu quedas tan tranquilo. Sin embargo, el lunes por la mañana  
el mismo gerente te solicita cambiar una parte del programa, ya que lo pensó  bien y realmente no le gustó el diseño final. Sin Git, tu tienes que regresar y borrar esas lineas de código manualmente e incluso podrías haber olvidado que habías escrito o qué es lo que tienes que borrar.  
En un ambiente laboral, son miles y miles de líneas ¿ya estas imaginando lo que vas a tardar cierto?  
Con Git, solamente hubieras tenido que ejecutar un par de comandos y voalá, viaje en el tiempo.  
¿Usarás Git de ahora en adelante?
Sí, leíste bien, con Git se viaja en el tiempo; claro, siempre y cuando sepas utilizarlo correctamente.

## Basta de trucos, enséñame Git y cómo utilizar Github

Supongamos situaciones críticas en un ambiente básico laboral

- WTF, soy nuevo en esto, ¿quien soy para Git? ¿le tengo que decir mi nombre o algo?  
> git config --global user.name "Juan Topo (aca pon tu nombre)"  
> git config --global user.email "juan@topos.com.mx"

- Empezaste un proyecto
> git init
- Escribiste un nuevo archivo, una clase, una interfaz, un lo que sea
> git add <nombre_del_archivo>
- No tengo idea que esta pasando
> git status
- ¿Escribiste varios y quieres meterlos todos de cajón?
> git add .  
> git add -a 
- Oops, no debiste colocar el archivo "ClaseSuperPrivada.cs" 
> git rm --cached <nombre_del_archivo>

Ahora sí, cuando tengas todos tus archivos en el stage
Espera ¿que es el stage?
Nada, sencillo, te lo pongo facil
Imagina que te vas a cambiar de casa, el stage es el camión que te ayuda a
subir todos los muebles; tu decides cuales se quedan y cuales se van.
Cuando ejecutas un commit, el camión se va con todo y muebles. 
Eso es un stage, un camión (no técnicamente, pero ya sabes, es algo así)


Ahora, un commit sería decirle al conductor del camión: "hey, llévate los muebles ya"
Un commit es un cambio o un punto de la historia dentro de tu rama maestra

- Realizaré mi primer commit ¿que debo hacer?
> git commit -m "Describe brevemente que hiciste"

- Rayos, no era la descripción correcta del ultimo commit que hice
> git commit --amend -m "Nuevo mensaje del ultimo commit"

Bien, haz hecho unos que otros commits, haz realizado ya muchos, de hecho

- Pff.. el jefe quiere que volvamos a realizar el diseño del programa .. ¿donde me quedó?
> git log   
> git log --oneline (Forma corta de ver las cadenas hash de tus commits)  
> git log --graph --decorate --oneline (Verlo super bonito y de manera jerarquica)  

- Vaaa, ya vi que commit fue el que es el del diseño ¿ahora que?
> git reset --hard <aqui_coloca_el_id_del_commit>  

- Vaya de perlas! Ahora mis archivos estan como en ese entonces, pero ... pf quiero volver a como estaba antes
> git reflog  

.  
.  
.
- Genial, solo tengo que buscar el commit indicado y ...
> git reset --hard <hash_del_commit_buscado>

- Raaaaayos, uno de los commits que hice tiene mal indicado el mensaje, de nuevo aqui vamos...
> git rebase -i HEAD~<n> (donde N es el numero de commits que quieres mostrar)  
> git rebase -i --root (TODOS los commits)

Renombra las palabras pick por reword y cambia el mensaje del commit  
Si tienes un editor, editalo y cierralo, veras reflejado los cambios en el CMD  

- Oye, y eso del "gitignore"  
El gitignore es un archivo que forma o no, parte de Git, y es donde tu escribes lo que quieres que Git IGNORE y no tengas problemas a la hora 
de agregarlo al staged area. Aqui suelen ir archivos binarios, ejecutables, algunas claves, tokens, documentos, builds, IDE settings, paths, etc.  
TU puedes agregar lo que quieras, si no quieres darle seguimiento a "ClaseNadaImportante.java"  
solo abre el gitignore en el bloc de notas, agregalo en una linea y voala...  Si tu gitignore no existe, agregalo manualmente

> [Mac/Linux] touch .gitignore  
> [Windows] cd> .gitignore (o bien utiliza el Git Bash haciendo clic derecho en tu ratón)

- Comandos demasiado largos y repetitivos? Sin apuros  
> git config --global alias.loquequieras "comandos"   
> git config --global alias.logbonito "git log --graph --decorate --oneline" <- te recomiendo mucho este :P

---  

Hasta aquí, estarías bien preparado para utilizar Git, mas NO estas utilizando GitHub  
Si solo deseas controlar tu programa o archivos en tu PC, basta con quedarte aquí, te lo aseguro.  
Sin embargo, es escencial utilizar GitHub  

¿Poooor?  
Porque a la hora de trabajar con amigos, colegas, compañeros, etc., estás obligado casi al cien porciento  
a trabajar en equipo, y si por azares del destino, Juanito hizo algo que no debía estar, puedes  
eliminarlo, puedes pedir que lo modifiquen, y lo mejooooooor de todo... las ramas! Con las ramas eres el  
maestro del tiempo y de los espacios, puedes tener mil distintas ramas de un solo programa y cuando decidas  
que lo que se haga en esas ramas es correcto, fusionarlas  

---  
