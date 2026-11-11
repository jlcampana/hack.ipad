# Jailbreak iPad Mini 2 (iOS 12.5.8) con Chimera — pasos en el Mac

Este USB contiene:
- **`ChimeraPatch-resigned.ipa`** → el jailbreak Chimera, build parcheado para A7 (tu iPad). Está en la raíz, junto a este archivo.
- **`jailbreak.md`** → esta guía.

> **Por qué en el Mac:** en Linux, Apple bloquea la firma gratuita (errores -80045/-80043) desde octubre 2026 y la herramienta de Linux está desactualizada. El Mac firma de forma **nativa**, así que esto funciona sin líos de "anisette".

---

## Antes de empezar (importante)

- Es un **Mac de trabajo**: si tiene gestión corporativa (MDM), puede **bloquear** instalar Sideloadly/AltServer. Si algo no deja instalarse, probablemente sea eso.
- Usa la **Apple ID nueva y dedicada**: `redes.squall209@passinbox.com` (la contraseña la tecleas tú; no está escrita aquí). **No** uses tu Apple ID personal ni la de trabajo.
- Ten el iPad y un **cable USB** a mano. El 2FA de la cuenta nueva llega por **SMS** a tu móvil.

---

## Opción recomendada: Sideloadly (lo más simple)

1. **Copia el IPA al Mac.** Arrastra `ChimeraPatch-resigned.ipa` de este USB al Escritorio del Mac.
2. **Descarga Sideloadly** desde [https://sideloadly.io](https://sideloadly.io) e instálalo (arrástralo a Aplicaciones). Si macOS se queja de "app no identificada": clic derecho → Abrir.
3. **Conecta el iPad al Mac** por USB. Si el iPad pregunta *¿Confiar en este ordenador?* → **Confiar** + tu código del iPad.
4. Abre **Sideloadly**:
   - Que detecte el iPad arriba (en el desplegable de dispositivo).
   - Arrastra `ChimeraPatch-resigned.ipa` a la ventana (o botón **IPA**).
   - En **Apple ID**: `redes.squall209@passinbox.com`.
   - Pulsa **Start**.
   - Pide la **contraseña** de esa Apple ID → la tecleas.
   - Pide **código 2FA** → te llega por **SMS** → lo escribes en el diálogo. (Si no llega: entra en appleid.apple.com en el navegador, inicia sesión con esa cuenta para forzar el envío del SMS, y vuelve a intentar.)
   - Espera a **"Done"** / instalación completada.

5. **Confía el certificado en el iPad:**
   Ajustes → General → **VPN y Gestión de dispositivos** → toca el perfil de `redes.squall209@...` → **Confiar**.

6. **Lanza el jailbreak:**
   Abre la app **Chimera** (icono nuevo en pantalla) → **Jailbreak** → el iPad reinicia → reabre **Chimera** → **Jailbreak** otra vez. Al terminar tendrás **Sileo** en la pantalla.

7. **Paquetes base (en Sileo):** instala en este orden:
   `libiosexec1` → luego `libhooker` → `PreferenceLoader` → `RocketBootstrap`.
   Reinicia SpringBoard si lo pide.

---

## Independencia (sin PC tras reiniciar)

Tu iPad es A7, así que **no necesitas re-firmar cada 7 días por PC**:

- Tras cualquier **reinicio en frío**, abre **Safari** en el iPad y entra en **`https://jbme.h4ck.kr`** → *re-jailbreak* → listo, **sin cable y sin Mac**.
- Guárdalo en favoritos de Safari.
- **El Mac ya no vuelve a hacer falta** después de esta primera instalación.

---

## Alternativa: AltServer (si Sideloadly falla)

1. Descarga **AltServer** desde [https://altstore.io](https://altstore.io).
2. Ábrelo → icono en la barra de menú → **Install AltStore** → elige el iPad → mete el Apple ID nuevo + 2FA.
3. En el iPad, confía el perfil (paso 5 de arriba) y abre **AltStore**.
4. En AltStore: pestaña **My Apps** → **+** (arriba izquierda) → elige `ChimeraPatch-resigned.ipa` → se instala.
5. Sigue desde el paso 5 (confiar) / 6 (jailbreak) de arriba.

---

## Si algo falla

- **"Unable to install" / error de firma:** cierra Sideloadly/AltServer y repite; asegúrate de usar la cuenta nueva.
- **No llega el SMS:** fuerza el login en appleid.apple.com con esa cuenta para que Apple lo mande, y reintenta rápido.
- **"Máximo de apps" (cuenta gratuita):** borra apps sideloaded previas; las gratuitas tienen límite de 3 apps activas.
- **MDM del Mac bloquea la instalación:** tendrías que usar otro Mac/PC Windows sin gestión corporativa.
- Apunta el error exacto y lo miramos juntos.

¡Suerte! Cuando Chimera diga "jailbroken", lo tienes.
