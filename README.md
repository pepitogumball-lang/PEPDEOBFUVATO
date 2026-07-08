# Custom Knight PEPDEOBFUVATO (Mobile Version)

Esta es una versión modificada de Custom Knight adaptada específicamente para **Hollow Knight en dispositivos móviles (Android/iOS)**.

## Cambios Realizados para Mobile
- **Eliminación de dependencias de escritorio:** Se han quitado las referencias a SDKs de Microsoft específicos de PC.
- **Compatibilidad con Unity Mobile:** El proyecto está configurado para usar librerías de Unity compatibles con Android/iOS.
- **Identificación Única:** Modificado para ser reconocido por el cargador de mods móvil como `Custom Knight PEPDEOBFUVATO`.
- **Estructura de Referencias:** Se utiliza una carpeta `References/` para las DLLs necesarias del juego móvil.

## Instalación en Mobile
1. Coloca la DLL compilada en la carpeta de mods de tu dispositivo (usualmente `Android/data/com.TeamCherry.HollowKnight/files/Mods`).
2. Asegúrate de tener instalada la dependencia **Satchel** versión móvil.
3. Reinicia el juego.

## Créditos
Basado en el trabajo original de [PrashantMohta](https://github.com/PrashantMohta/HollowKnight.CustomKnight).

## Automatización con GitHub Actions
He configurado un workflow en `.github/workflows/android.yml` que:
1. Prepara el entorno .NET.
2. Intenta compilar el mod en modo Release.
3. Genera un artefacto descargable con la DLL final.

**Nota Importante:** Para que el workflow funcione en GitHub, debes subir las DLLs de referencia (UnityEngine, Assembly-CSharp, etc.) a la carpeta `References/` del repositorio, ya que son necesarias para la compilación.
