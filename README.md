# CoinOPS ES-X
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/d6b03f45-cd3b-44d6-856b-d68a3a2bd473" />

Adaptación del tema **CoinOPS** para [EmulationStation-X](https://github.com/Renetrox/EmulationStation-X).

Esta versión conserva la estética de gabinete/televisor y la rueda de logos de CoinOPS, pero fue reorganizada para aprovechar las funciones propias de ES-X. No es una copia directa del tema para ES-DE ni requiere sus variantes.

## Características

### Vista de sistemas

- Carrusel horizontal de tres sistemas.
- Sistema seleccionado alineado con la ilustración de su control.
- Fanart y descripción propios de cada plataforma.
- Logo, contador de juegos y arte del control.
- Reloj e indicadores de red y Bluetooth integrados en la esquina superior izquierda.
- Recursos dinámicos mediante `${system.theme}`.

### Lista de juegos

- Rueda vertical curva basada en el carrusel nativo de ES-X.
- Logos *marquee* y nombre del juego como alternativa cuando no existe una imagen.
- Vídeo con captura como alternativa.
- Fanart, gabinete o televisor y carátula.
- Título y descripción en blanco con contorno negro para conservar la legibilidad sin cubrir el gabinete con un panel.
- Valoración, jugadores, desarrollador, editor, fecha, veces jugado y última partida.
- Iconos compactos para la metadata.
- Gabinete genérico cuando el sistema no dispone de uno propio.
- Compatible con las vistas `basic`, `detailed` y `video`.

## Compatibilidad

El tema está desarrollado y probado para **EmulationStation-X** en formato **16:9**.

Varias propiedades utilizadas por la rueda —como `carouselMode`, `carouselItemRotation`, `logoSpacingY`, `logoOffsetX` y el texto alternativo condicional— dependen de las extensiones incorporadas en ES-X. Por ese motivo, el funcionamiento completo no está garantizado en otras variantes de EmulationStation.

## Instalación

Clona el repositorio dentro de la carpeta de temas de EmulationStation:

```bash
cd ~/.emulationstation/themes
git clone https://github.com/Renetrox/coinops-es-x.git
```

Después, abre EmulationStation-X y selecciona **coinops-es-x** en las opciones de interfaz.

Para actualizar una instalación existente:

```bash
cd ~/.emulationstation/themes/coinops-es-x
git pull
```

## Multimedia recomendada

Para aprovechar todo el diseño, cada juego puede incluir:

- Logo o *marquee*.
- Vídeo.
- Captura de pantalla.
- Fanart.
- Carátula o miniatura.
- Metadata: valoración, jugadores, desarrollador, editor, fecha, contador de partidas y última partida.

Si un juego no tiene *marquee*, ES-X muestra su nombre en la rueda. Si no tiene vídeo, puede mostrar su captura. La disponibilidad final depende de los medios registrados en el `gamelist.xml`.

## Estructura de recursos por sistema

El tema busca los recursos usando el identificador `${system.theme}`:

```text
_inc/systems/fanart/<sistema>.jpg
_inc/systems/logos/<sistema>.png
_inc/systems/logos/<sistema>.svg
_inc/systems/cabinets/<sistema>.png
_inc/systems/system-controllers-outline/<sistema>.svg
_inc/systems/system-metadata/<sistema>.xml
```

El nombre de cada archivo debe coincidir exactamente con el identificador del tema asignado al sistema. Esto también se aplica a sistemas personalizados y colecciones.

## Créditos

- Tema y concepto original de CoinOPS: **BritneysPAIRS (BP)**.
- Arte de gabinetes y televisores: **gjsmsmith**.
- Base del tema CoinOPS para ES-DE: **TheGrizzMD**.
- Logos e ilustraciones de sistemas basados en [Alekfull ARTFLIX](https://github.com/fagnerpc/Alekfull-ARTFLIX/) y [ARTFLIX-Cobalto](https://github.com/galisteogames/ARTFLIX-Cobalto/).
- Adaptación, integración y ajustes para EmulationStation-X: **Renetrox**.

Si falta alguna atribución, puedes comunicarlo mediante un *issue* para corregirla.

## Licencia

Este proyecto se distribuye bajo **Creative Commons Attribution-NonCommercial-ShareAlike 2.0 (CC BY-NC-SA 2.0)**.

Puedes compartir y adaptar el tema siempre que mantengas la atribución, no lo utilices con fines comerciales y distribuyas las modificaciones bajo la misma licencia.

Consulta los términos completos en [Creative Commons](https://creativecommons.org/licenses/by-nc-sa/2.0/).
