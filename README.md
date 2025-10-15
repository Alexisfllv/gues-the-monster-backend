# 🚀 Reglas y Flujo de Trabajo - Equipo Backend

## 🧩 Estructura del Repositorio
- **Ramas principales:**
  - `main` → código estable (producción)
  - `develop` → integración de nuevas funciones (desarrollo)
- **Ramas temporales (de cada integrante):**
  - `feature/` → nuevas funcionalidades
  - `fix/` → corrección de errores
  - `hotfix/` → arreglos urgentes sobre `main`

---

## 🔄 Flujo de Trabajo (Git Flow Simplificado)
1. Clonar el repositorio:
   ```bash
   git clone <URL-del-repo>
   git checkout develop
   git pull
   ```

2. Crear tu rama desde `develop`:
   ```bash
   git checkout -b feature/nombre-funcionalidad
   ```

3. Trabajar y realizar commits siguiendo el formato de **Conventional Commits**.

4. Subir tu rama:
   ```bash
   git push origin feature/nombre-funcionalidad
   ```

5. Abrir un **Pull Request → `develop`**  
   - El PR debe tener una descripción clara.  
   - No hacer push directo a `develop` o `main`.

6. Esperar revisión y aprobación del líder antes del merge.

7. Cuando `develop` esté estable → se hace merge a `main` para producción.

---

## 🏷️ Naming Conventions
Usar nombres cortos, claros y en minúsculas:
- `feature/login-api`
- `feature/crear-evento`
- `fix/error-validacion`
- `hotfix/bug-deploy`

---

## ✍️ Conventional Commits
Formato:  
```
<tipo>: <descripción corta>
```

**Tipos más usados:**
- `feat:` nueva funcionalidad  
- `fix:` corrección de error  
- `refactor:` mejora de código sin cambiar funcionalidad  
- `docs:` cambios en documentación  
- `style:` formato o estilo (espacios, comas, etc.)  
- `test:` agregar o modificar pruebas  

**Ejemplos:**
```bash
git commit -m "feat: agregar endpoint para crear usuario"
git commit -m "fix: corregir validación de correo"
```

---

## 🧠 Buenas Prácticas
- Pull frecuente desde `develop` para evitar conflictos:
  ```bash
  git pull origin develop
  ```
- Commits pequeños y descriptivos.  
- Revisar y comentar PRs de otros.  
- No trabajar nunca directamente en `develop` ni `main`.  
- Resolver conversaciones antes de hacer merge.

---

## 👑 Roles
- **Líder Backend:** controla merges a `develop` y `main`.  
- **Colaboradores:** crean ramas, hacen PRs y esperan aprobación.

---

**💬 Recordatorio:**  
El orden, los nombres y las revisiones garantizan un flujo limpio, colaborativo y sin conflictos.  
Cualquier duda, consultarla antes de hacer un merge.

