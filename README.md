# VB6-Ejecutables

Distribución de los **ejecutables firmados** de los programas Doscar/Prosicar para el
programa actualizador. Repo **público** (descarga raw).

## Estructura

Una carpeta por programa. Dentro de cada una:

- `NN.AAMM.DD_<exe>.zip` — **cada** versión compilada a producción, siempre con su fecha (exe firmado + notas `.txt`). El último también va datado: no hay copias sin fecha.
- `ULTIMA.txt` — **puntero de nombre fijo**: contiene el nombre del zip más reciente. **Es lo que lee el actualizador.**

```
barRestaurante/
├─ 11.2606.22_bar.zip      (versión datada)
├─ 11.2606.23_bar.zip      (versión datada = la actual)
└─ ULTIMA.txt              (→ "11.2606.23_bar.zip")
```

El actualizador hace **dos pasos** (mismo patrón que `controlLibrerias`):

1. Lee el puntero (URL fija):
   `https://raw.githubusercontent.com/grupodoscar-bot/VB6-Ejecutables/main/<carpeta>/ULTIMA.txt`
2. Descarga el zip datado que indica:
   `https://raw.githubusercontent.com/grupodoscar-bot/VB6-Ejecutables/main/<carpeta>/<contenido-de-ULTIMA.txt>`

Así todas las versiones quedan controladas con su fecha y la URL que consulta el actualizador sigue siendo fija.

Programas: `barRestaurante`, `gestion`, `peluqueria`, `taller`, `tpv`, `carpintero`, `cristaleria`.

> El contenido se publica mediante un proceso interno automatizado. **No editar a mano.**
