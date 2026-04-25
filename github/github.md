## Git & GitHub — Resumen práctico

### Configuración inicial (una sola vez)

bash

```bash
git config --global user.name "TuNombre"
git config --global user.email "tuemail@gmail.com"
git config --list  # verificar que quedó bien
```

### Clonar un repositorio

bash

```bash
git clone https://github.com/usuario/repo.git
cd repo
code .  # abrir en VS Code
```

### Ciclo de trabajo diario

bash

```bash
git status              # ver qué cambió
git add archivo.txt     # preparar un archivo
git add .               # preparar todos los archivos
git commit -m "mensaje" # guardar snapshot
git push                # subir a GitHub
git pull                # bajar cambios del remoto
```

### Ramas

bash

```bash
git checkout -b feature/nombre   # crear rama y moverse a ella
git push -u origin feature/nombre # subir rama por primera vez
git push                          # siguientes veces
```

### Flujo completo con ramas

```
1. git checkout -b feature/nueva
2. hacer cambios
3. git add .
4. git commit -m "descripción"
5. git push -u origin feature/nueva
6. Abrir Pull Request en GitHub
7. Merge pull request
8. Delete branch
```

### Conceptos clave

- **main** — rama principal, código estable
- **rama** — copia paralela para trabajar sin afectar main
- **commit** — snapshot del proyecto en un momento
- **push** — subir commits locales a GitHub
- **pull** — bajar commits remotos a tu máquina
- **Pull Request** — solicitud para fusionar una rama con main
- **Merge** — fusionar los cambios de una rama a otra
- **origin** — nombre por defecto del repositorio remoto

### Zonas de Git

```
[Archivos]  →  git add  →  [Staged]  →  git commit  →  [Historial]
```

---

Todo esto lo practicaste hoy con tu repo `mi-primer-repo`. 💪