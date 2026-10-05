# Workflow Benchmarks 🦈

Repositorio para pruebas de rendimiento y automatización de flujos CI/CD con GitHub Actions.

## Configuración Requerida en GitHub

Para que el workflow funcione sin errores de permisos y los Pull Requests se atribuyan a tu cuenta:

### 1. Permisos de GitHub Actions en el Repositorio
Ve a: **Settings** > **Actions** > **General**
* En **Workflow permissions**, selecciona: `Read and write permissions`.
* Marca la casilla: `Allow GitHub Actions to create and approve pull requests`.
* Guarda los cambios (**Save**).

### 2. Atribución del logro (Personal Access Token - Recomendado)
Por defecto, si se usa el token interno de GitHub (`GITHUB_TOKEN`), el autor del PR será `github-actions[bot]`. Para que GitHub acredite los PRs a **tu cuenta** y desbloquee el logro **Pull Shark**:
1. Ve a tu perfil > **Settings** > **Developer Settings** > **Personal access tokens** (Tokens Classic).
2. Genera un nuevo token con permisos `repo` y `workflow`.
3. En este repositorio, ve a **Settings** > **Secrets and variables** > **Actions**.
4. Crea un nuevo Secret llamado `GH_PAT` con el valor del token creado.

*(Si no configuras `GH_PAT`, el workflow usará `GITHUB_TOKEN` de forma predeterminada).*

## Cómo ejecutar

1. Ve a la pestaña **Actions** de este repositorio.
2. Selecciona **Pull Shark Automation** en el panel izquierdo.
3. Haz clic en **Run workflow**.
4. Elige la cantidad de PRs (se recomienda ejecutar en tandas de 50 o 100).
