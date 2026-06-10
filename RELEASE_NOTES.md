# 📦 Release Notes

---

## v1.0 — 2026-06-10

### 🎉 Primera versión pública

Primera versión de **Autodesk-Cleaner-Enterprise**, fork empresarial de Autodesk-Nuke v6.3.

### ✨ Novedades respecto al original

- Perfil de limpieza único **ENTERPRISE** optimizado para entornos empresariales
- Limpieza multi-usuario: procesa `NTUSER.DAT` de todos los perfiles del equipo
- Kill forzado de servicios via **CIM** para procesos resistentes
- Reparación de bucles de reinicio: filtra entradas de Autodesk en `PendingFileRenameOperations` sin afectar el resto del sistema
- Limpieza de variables de entorno del sistema (`ADSK_LICENSE_FILE`, `PATH`, etc.)
- Verificación post-limpieza exhaustiva con reporte detallado
- Log completo con timestamps en `%TEMP%`
- Modo `-DryRun` para simular la ejecución sin cambios reales
- Confirmación manual obligatoria antes de ejecutar (`LIMPIAR ENTERPRISE`)

### 🛠 Productos cubiertos

`Autodesk` `AutoCAD` `Revit` `Inventor` `Fusion 360` `Civil 3D` `Maya` `3ds Max`

### 📋 Basado en

Autodesk-Nuke Fusion (v2.0.2, v3.0-OOP, v4.0, v5.0, v6.0, v6.2, v6.3) por jcieza
