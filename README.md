# VB6-Ejecutables

Distribución de los **ejecutables firmados** de los programas Doscar/Prosicar para el
programa actualizador. Repo **público** (descarga raw).

## Estructura

Una carpeta por programa. Dentro de cada una:

- `NN.AAMM.DD_<exe>.zip` — histórico: cada versión compilada a producción (exe firmado + notas `.txt`).
- `<carpeta>.zip` — **copia del último zip** (nombre fijo). **Es lo que descarga el actualizador.**

```
barRestaurante/
├─ 11.2606.22_bar.zip      (histórico)
├─ 11.2606.23_bar.zip      (histórico)
└─ barRestaurante.zip      (= último → URL fija del actualizador)
```

URL fija de descarga (raw):
`https://raw.githubusercontent.com/grupodoscar-bot/VB6-Ejecutables/main/<carpeta>/<carpeta>.zip`

Programas: `barRestaurante`, `gestion`, `peluqueria`, `taller`, `tpv`, `carpintero`, `cristaleria`.

> El contenido se publica mediante un proceso interno automatizado. **No editar a mano.**
