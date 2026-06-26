# Comandos de Git

## 1 - `git init`

- Inicializa un nuevo repositorio Git en la carpeta actual.
- Crea la carpeta oculta `.git` donde se guarda toda la información del control de versiones.

---

## 2 - Ramas en Git

- Una rama es una línea de desarrollo independiente.
- `master` o `main` suele ser la rama principal.
- Se usan para trabajar en nuevas funcionalidades sin afectar el código estable.

---

## 3 - `git add` y `git commit`

- `git add <archivo>` → prepara cambios para ser guardados (stage).
- `git commit -m "mensaje"` → guarda los cambios en el historial del repositorio.

---

## 4 - `git log` y `git status`

- `git log` → muestra el historial de commits.
- `git status` → indica el estado actual de los archivos (modificados, preparados, sin seguimiento).

---

## 5 - `git checkout` y `git reset`

- `git checkout <rama|commit>` → moverte a otra rama o commit.
- `git reset <commit>` → deshace cambios, moviendo HEAD a un commit anterior.
  - `--soft` → mantiene cambios en staging.
  - `--hard` → borra cambios y regresa al commit exacto.

---

## 6 - `git alias`

- Permite crear atajos para comandos largos.
- Ejemplo:

```bash
git config --global alias.lg "log --oneline --graph --decorate"
```

---

## 7 - Fichero `.gitignore`

- Archivo especial donde defines qué ficheros o carpetas no deben ser rastreados por Git.
- Útil para excluir archivos temporales, configuraciones locales o dependencias externas.
- Ejemplo típico:

```bash
node_modules/
*.log
.env
```

---

## 8 - `git diff`

- Muestra las diferencias entre el estado actual y el último commit.
- Permite ver qué líneas fueron añadidas, eliminadas o modificadas.
- Ejemplo:

```bash
git diff
```

---

## 9 - Desplazamiento en una rama

- Usar `git checkout <rama>` para moverte entre ramas.
- Permite trabajar en diferentes versiones del proyecto sin mezclar cambios.
- Ejemplo:

```bash
git checkout develop
```

---

## 10 - `git reset --hard` y `git reflog`

- `git reset --hard <commit>` → regresa la rama al commit indicado, borrando cambios en staging y en el directorio de trabajo.
- `git reflog` → muestra el historial de movimientos de HEAD (incluye cambios de rama, resets y commits).
- Ejemplo:

```bash
git reset --hard abc123
git reflog
```

---

## 11 - `git tag`

- Sirve para marcar commits importantes, como versiones de lanzamiento.
- Se pueden crear tags ligeros o anotados.
- Ejemplo:

```bash
git tag v1.0.0
git push origin v1.0.0
```

## 12 - `git branch y switch`