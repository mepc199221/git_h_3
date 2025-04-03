🏆 H-3 (HACER MERGE EN MI MASTER LOCAL Y LUEGO CON MASTER REMOTO)


| Hacks  | Details |
|--------|------|
| H-3    | 	Hacer merge en mi master local y luego con master remoto   |

1. Crear un nuevo repositorio en github nombre:`git_h_3`.

2. Crear un repositorio local
git init

3. Registrar el repositorio remoto con tú repositorio local
git remote add origin (pegar_la_ruta_del_repositorio_local)

4. Verificamos la ruta remota
git remote -v

5. Se te asigna una tarea de crear una lista de comidas, para tal fin hacemos un archivo llamado "menu_de_comidas.txt"
touch menu_de_comidas

6. Verificamos que el archivo existe en nuestro equipo y adicional examinamos el estatus en git
ls -l
git status

7. Agregamos el archivo, verificamos su status de stage y log, para luego hacer push
git add .
git status
git commit -m "feat: add menu_de_comidas.txt"
git log --oneline
git push -u origin master

8. Toca analizar el repositorio remoto en github para ver el commit

9. Se necesita crear una rama llamada feature/agregarComidas
git branch feature/agregarComidas

10. Comprobar la creación de la rama
git branch 

11. Como se trata de agregar comida al archivo "menu_de_comidas.txt" lo ideal que para cada tarea a realizar se cree una nueva rama, bien vamos a la rama creada
 git switch feature/agregarComidas

12. Ahora agregamos una lista de comidas al archivo "menu_de_comidas.txt", esto se hace por medio del comando echo -e "mas el texto"
echo -e "arroz, pan, pizza" >> menu_de_comidas.txt

13. Se necesita observar dentro del archivo "menu_de_comidas.txt" para ver el contenido anexado
cat menu_de_comidas.txt

14. Viendo que hemos logrado anexar un contenido al archivo, vamos a crear un commit
git status
git add .
git status
git commit -m "feat: add content in menu_de_comidas.txt"
git log --oneline

15.Cuando se tiene la tarea lista, se retorna a la rama master
git switch master

16.Observa que estas en la rama principal (master)
git branch 

17.Anexamos la tarea que esta en la rama "feature/agregarComidas" al master, mediante el comando merge y de esta forma actualizamos el área de trabajo llamado master(es decir la rama master)
git merge feature/agregarComidas

18.Trasladamos la tarea a la rama master del repositorio remoto
git push -u origin master

19.Miramos el repositorio remoto y ver si todo esta bien.

20.Volvemos a la consola y observamos nuestras ramas
git branch 

21.Podemos dejar la rama "feature/agregarComidas", como un mecanismo de respaldo aunque sino lo deseamos también puedes eliminarla
git branch -D feature/agregarComidas

22.Exploramos las ramas
git branch


