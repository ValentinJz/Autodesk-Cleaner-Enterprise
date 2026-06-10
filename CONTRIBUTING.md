# 🤝 Contribuciones

¡Gracias por tu interés en mejorar Autodesk-Cleaner-Enterprise!

---

## 🐛 Reportar un bug

Si encontraste un problema, abrí un **Issue** en GitHub con la siguiente información:

- Versión de Windows
- Versión de PowerShell (`$PSVersionTable.PSVersion`)
- Productos de Autodesk que intentabas desinstalar
- Descripción del problema
- Contenido del archivo `.log` generado en `%TEMP%`

---

## 💡 Proponer una mejora

Si tenés una idea para mejorar el script, abrí un **Issue** con la etiqueta `enhancement` y describí:

- Qué querés agregar o cambiar
- Por qué sería útil en entornos empresariales
- Si ya tenés código, podés abrir un **Pull Request**

---

## 🔧 Pull Requests

1. Hacé un fork del repositorio
2. Creá una rama con un nombre descriptivo: `fix/problema` o `feature/mejora`
3. Realizá tus cambios
4. Probá el script en modo `-DryRun` antes de enviar
5. Abrí el Pull Request describiendo qué cambiaste y por qué

---

## 📌 Consideraciones

- El script está pensado para entornos empresariales, priorizá la seguridad y estabilidad
- No eliminar archivos personales del usuario es una regla no negociable
- Cualquier cambio destructivo debe estar cubierto por el modo `-DryRun`
- Comentá el código en español para mantener consistencia
