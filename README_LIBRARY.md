# Componentes UI - Biblioteca

Uso rápido para consumir la librería desde otro proyecto:

- Instala desde npm: `npm i componentes-ui` (o usa la ubicación privada que prefieras).

Exportaciones principales:

- `THEME`: preset de colores por defecto (export por defecto también).
- `NAV_THEME`: preset para `@react-navigation/native`.
- `createThemeWithOverrides(overrides?)`: crea un theme combinado donde puedes pasar colores personalizados por `light` y/o `dark`.
- Componentes: `Text`, `Button`, `Icon`.

Ejemplo de override de colores:

```ts
import { createThemeWithOverrides } from 'componentes-ui';

const { theme, navTheme } = createThemeWithOverrides({
  light: {
    primary: '#0ea5e9',
    background: '#ffffff'
  }
});

// Pasa `navTheme.light` a NavigationContainer
```

Notes:

- La librería externaliza `react`, `react-native`, `lucide-react-native` y `@react-navigation/native` para evitar bundling.
- Si necesitas más mezcla profunda (nested objects), modifica `createThemeWithOverrides`.
