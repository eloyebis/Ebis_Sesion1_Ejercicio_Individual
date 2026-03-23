# 🚀 Repositorio Experimental - Taller de Git & GitHub

Bienvenido a este repositorio experimental. En este taller aprenderás los conceptos básicos de Git y GitHub practicando con un flujo de trabajo estándar.

## 📋 Objetivo

Cada alumno debe:
1. Crear una rama personal
2. Añadir un archivo `.txt` con su nombre de usuario de GitHub
3. Crear una Pull Request (PR) hacia la rama `main`

## 🎯 Pasos a Seguir

### Paso 1: Clonar el Repositorio

```bash
git clone <URL del repositorio>
cd <nombre del repositorio>
```

### Paso 2: Crear una Rama Personal

Crea una rama con tu nombre de usuario de GitHub (usa `-` en lugar de espacios):

```bash
git checkout -b usuarios/tu-usuario-github
```

**Ejemplo:**
```bash
git checkout -b usuarios/juan-perez
```

### Paso 3: Crear tu Archivo .txt

En la raíz del repositorio, crea un archivo con tu nombre de usuario:

```bash
echo "Hola, soy tu-usuario-github" > tu-usuario-github.txt
```

**Ejemplo:**
```bash
echo "Hola, soy juan-perez" > juan-perez.txt
```

### Paso 4: Agregar Contenido (Opcional)

Puedes añadir información adicional en tu archivo:

```bash
cat >> tu-usuario-github.txt << EOF

Email: tu-email@ejemplo.com
Fecha: $(date)
Curso: Taller de Git
EOF
```

### Paso 5: Confirmar los Cambios (Commit)

Añade el archivo a staging y crea un commit:

```bash
git add tu-usuario-github.txt
git commit -m "feat: Añadir tu-usuario-github al repositorio"
```

**Ejemplo de mensaje de commit:**
```bash
git commit -m "feat: Añadir juan-perez al repositorio"
```

### Paso 6: Subir los Cambios (Push)

Sube tu rama al repositorio remoto:

```bash
git push origin usuarios/tu-usuario-github
```

### Paso 7: Crear una Pull Request

1. Ve a GitHub y abre el repositorio
2. Verás un banner sugiriendo crear una PR para tu rama reciente
3. Haz clic en **"Compare & pull request"**
4. Completa el formulario:
   - **Título:** `Añadir usuario: tu-usuario-github`
   - **Descripción:** Breve descripción de ti (nombre real, carrera, etc.)
5. Asegúrate de que:
   - La rama base es `main`
   - Tu rama es `usuarios/tu-usuario-github`
6. Haz clic en **"Create pull request"**

## 📝 Plantilla de Descripción de PR

```markdown
## 📌 Descripción
He añadido mi usuario al repositorio como parte del taller de Git.

## 👤 Información Personal
- **Nombre Completo:** Tu Nombre
- **Usuario GitHub:** tu-usuario-github
- **Carrera/Programa:** Tu Carrera
- **Email:** tu-email@ejemplo.com

## ✅ Checklist
- [x] He creado el archivo .txt con mi nombre de usuario
- [x] He usado la rama `usuarios/tu-usuario-github`
- [x] He escrito un commit message claro
```

## 🔍 Verificar tu Trabajo

Una vez creada la PR, verifica:

```bash
# Ver el estado de tu rama
git status

# Ver el historial de commits
git log --oneline

# Ver las ramas locales
git branch -a
```

## ❓ Solución de Problemas

### Problema: "Permission denied (publickey)"
**Solución:** Configura tu SSH key en GitHub
```bash
ssh-keygen -t ed25519 -C "tu-email@ejemplo.com"
# Añade la clave pública en GitHub Settings > SSH keys
```

### Problema: "Upstream branch conflicted"
**Solución:** Actualiza tu rama desde `main`
```bash
git fetch origin
git rebase origin/main
git push origin usuarios/tu-usuario-github --force
```

### Problema: "No cambios en la rama"
**Solución:** Verifica que has hecho commit
```bash
git status  # Debe mostrar "working tree clean"
git log     # Debe mostrar tu commit
```

## 📚 Recursos Útiles

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Conventional Commits](https://www.conventionalcommits.org/)

## 🎓 Conceptos Clave Aprendidos

- ✅ Clonar repositorios
- ✅ Crear y cambiar ramas
- ✅ Hacer commits
- ✅ Push a repositorio remoto
- ✅ Crear Pull Requests
- ✅ Colaboración en equipo

---

**¡Felicidades! 🎉 Has completado el taller cuando tu PR sea mergeada a `main`.**

Si tienes dudas, contacta con tu instructor o abre un issue en este repositorio.
