# Marte Medieval Avanzado (Unity)

Pequeña escena explorable: terreno tipo Marte con rocas, árboles y una aldea (decorativa).
Pensada como práctica del taller realizado en clases en Unity.

---

## 1) Cómo abrir el proyecto

**Opción A – Clonar**
1. `git clone https://github.com/RicardoHerrera2004/Desarrollo_de_terrenos.git`
2. Unity Hub → **Open** → selecciona la carpeta clonada.
3. Abre la escena: `Assets/Scenes/SampleScene.unity`.

**Opción B – ZIP (descarga estándar de GitHub)**
1. En GitHub → botón **Code → Download ZIP** y descomprime.
2. Unity Hub → **Open** → carpeta descomprimida.
3. Abre `Assets/Scenes/SampleScene.unity`.

**Opción C – Descarga directa del paquete .7z (RECOMENDADA en este repo)**
> En este repositorio está subido `Desarrollo_De_Terrenos.7z` con **solo** `Assets/`, `Packages/` y `ProjectSettings/`.

1. En la página del repo, haz clic en **`Desarrollo_De_Terrenos.7z`**.
2. Pulsa **Download raw** (o el botón **Download** si aparece).
3. Descomprime el `.7z` (con 7-Zip o similar) en una carpeta nueva.
4. Unity Hub → **Open** → selecciona esa carpeta.
5. Abre la escena: `Assets/Scenes/SampleScene.unity`.

> Alternativa futura: si el archivo se publica en **Releases**, entra a la pestaña **Releases** del repo y descarga la última versión (vX.Y).

---

## 2) Cómo ejecutar

1. Abre la escena principal.
2. Pulsa **Play** en la barra superior del Editor.

La cámara arranca mirando el terreno; no hay controles de personaje.

---

## 3) Navegación por la escena (controles)

Este proyecto incluye **cámara libre** para moverse por el escenario en *Play*.
El script está en `Assets/Scripts/FlyCamera.cs` y va en la **Main Camera**.

**FlyCamera (estilo “volar”)**
- **Mantén botón derecho** del ratón para **mirar**.
- **W / A / S / D**: avanzar / izquierda / retroceder / derecha.
- **Q / E**: bajar / subir.
- **Shift**: más rápido · **Ctrl**: más lento.
- **Rueda** del ratón: ajusta la velocidad de movimiento.
- La cámara intenta mantenerse **por encima del terreno** para no atravesarlo.

> Prefieres orbitar un punto fijo (tipo RTS)? Activa `OrbitCamera.cs`
> (si está en el proyecto) en la Main Camera y asigna el **target** (un Empty en el centro):
> - **RMB**: orbitar · **MMB**: pan · **Rueda**: zoom.

---

## 4) Estructura del proyecto
Assets/
├─ Scenes/ # Escenas (.unity) → abrir "SampleScene.unity"
├─ Scripts/ # FlyCamera.cs (y/o OrbitCamera.cs)
├─ Models/ # Modelos 3D (dragón, rocas, árboles, props, etc.)
├─ Materials/
└─ Textures/
Packages/ # Paquetes usados por Unity
ProjectSettings/ # Ajustes del proyecto


---

## 5) Notas

- Si Unity pregunta por versión, usa la misma con la que se creó el proyecto (recomendado 2022.3 LTS o superior compatible).
- Si al abrir faltan paquetes, ve a **Window → Package Manager** y deja que Unity los resuelva.
- El paquete `.7z` **no** incluye `Library/`, `Temp/`, `Builds/`, etc. (se regeneran automáticamente).


