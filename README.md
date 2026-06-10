# 🧹 Autodesk-Cleaner-Enterprise

> Herramienta de limpieza profunda de Autodesk, diseñada específicamente para entornos empresariales.

Basado en [Autodesk-Nuke v6.3](https://github.com/jcieza/Autodesk-Nuke-A-Autodesk-Clean-Uninstall-Tool/) por **jcieza**, reescrito y adaptado para resolver los casos más complejos y problemáticos en empresas.

---

## 🎯 ¿Por qué esta versión?

Esta herramienta nació de una necesidad real en un entorno empresarial.

Antes de su existencia, la solución ante problemas graves de Autodesk era formatear el equipo directamente. Con el tiempo esto se volvió inviable por la constante pérdida de información que generaba.

Fue entonces cuando descubrí **Autodesk-Nuke**, una excelente herramienta que me dio la base para construir esta versión. La adapté y ajusté para las necesidades específicas de la empresa, con foco en hacer el proceso más guiado e intuitivo tanto para el equipo técnico como para usuarios finales que pudieran necesitar ejecutarla.

### 🔭 A futuro
- Incorporar nuevas carpetas y rutas de instalación a medida que Autodesk las modifica
- Mejorar la cobertura de limpieza en cada versión
- Optimizar y simplificar el código

---

## ⚠️ Advertencia

> **Este script realiza cambios IRREVERSIBLES en el sistema.**
> Si bien no elimina archivos personales ni `.DWG` del sistema, **sí elimina las carpetas de Autodesk en su totalidad.**
> Se recomienda mover cualquier archivo personal fuera de dichas carpetas antes de continuar.

---

## 📋 Requisitos

- Windows 10 / 11
- PowerShell 5.1 o superior
- Ejecutar como **Administrador**

---

## ✨ ¿Qué hace?

Encuentra y elimina cualquier rastro de: `Autodesk` `AutoCAD` `Revit` `Inventor` `Fusion` `Civil 3D` `Maya` `3ds Max`

| Paso | Acción |
|------|--------|
| 1 | Detiene todos los procesos y servicios de Autodesk |
| 2 | Desinstala paquetes MSI, ODIS, AdskUninstallHelper, Licensing, Identity Manager |
| 3 | Limpia registro HKLM, HKCU, HKCR, Installer\Products |
| 4 | Elimina todas las carpetas conocidas incluyendo Common Files, Public, Temp |
| 5 | Limpia perfiles de usuario y NTUSER.DAT de todos los usuarios del equipo |
| 6 | Elimina tareas programadas relacionadas a Autodesk |
| 7 | Repara bucles de reinicio (PendingFileRename + RebootRequired) |
| 8 | Limpia variables de entorno del sistema |

---

## 🚀 Uso

### Ejecución normal
```powershell
powershell.exe -ExecutionPolicy Bypass -File "Autodesk-Cleaner-Enterprise-v1.0.ps1"
```

### Modo simulación (sin cambios reales)
```powershell
powershell.exe -ExecutionPolicy Bypass -File "Autodesk-Cleaner-Enterprise-v1.0.ps1" -DryRun
```

### Modo silencioso (solo logs a archivo)
```powershell
powershell.exe -ExecutionPolicy Bypass -File "Autodesk-Cleaner-Enterprise-v1.0.ps1" -QuietMode
```

### Log personalizado
```powershell
powershell.exe -ExecutionPolicy Bypass -File "Autodesk-Cleaner-Enterprise-v1.0.ps1" -LogPath "C:\Logs\limpieza.log"
```

---

## 📁 Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------|-------------|
| `-DryRun` | Switch | Simula la ejecución sin realizar cambios reales |
| `-LogPath` | String | Ruta personalizada para el archivo de log |
| `-SkipValidation` | Switch | Omite las validaciones iniciales (solo para testing) |
| `-QuietMode` | Switch | Reduce el output en consola, escribe solo al log |

---

## 📊 Reporte final

Al terminar, el script genera un reporte con:

- Procesos y servicios detenidos
- Paquetes desinstalados
- Claves de registro eliminadas
- Carpetas eliminadas
- Tareas programadas removidas
- Variables de entorno limpiadas
- Errores y advertencias encontradas
- Ruta del archivo de log generado

---

## 🔒 Seguridad

- Requiere confirmación manual escribiendo `LIMPIAR ENTERPRISE` antes de ejecutar
- Modo `-DryRun` disponible para revisar cambios antes de aplicarlos
- Log completo guardado en `%TEMP%` por defecto
- No elimina archivos `.DWG` ni documentos personales del sistema

---

## 📝 Créditos

Este proyecto está basado en **[Autodesk-Nuke](https://github.com/jcieza/Autodesk-Nuke-A-Autodesk-Clean-Uninstall-Tool/)** de **jcieza / Dealis-SSM**.

Modificado y adaptado para entornos empresariales por **ValentinJz**.

---

## 📄 Licencia

Distribuido bajo licencia MIT. Ver [`LICENSE`](LICENSE) para más información.
