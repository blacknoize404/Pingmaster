# Pingmaster

> **Un monitor de escritorio para hosts y API**: hace ping a un destino según un intervalo, muestra el
> historial de latencia en vivo y te avisa en cuanto se cae. Vive en la bandeja del sistema y no molesta.
> Funciona en Windows y Linux.

<p align="center">
  <img src="docs/images/pingmaster-landing.png" alt="Vista principal de Pingmaster, con los botones de iniciar monitorización y ajustes" width="32%">
  <img src="docs/images/pingmaster-timeout.png" alt="Vista de estadísticas de Pingmaster, con la gráfica de tiempos de respuesta" width="35%">
  <img src="docs/images/pingmaster-settings.png" alt="Vista de ajustes de Pingmaster: host, tipo de petición y tiempos" width="32%">
</p>

## Qué hace

- **Monitorización continua.** Elige un host o un endpoint de API y Pingmaster lo sondea según un
  intervalo configurable: HTTP, HTTPS, ICMP o ICMP nativo.
- **Estadísticas de latencia.** Una gráfica deslizante con los tiempos de respuesta por host, además del
  método y el estado de respuesta actuales de un vistazo.
- **Notificaciones en bandeja.** Avisos emergentes de Windows y un sonido cuando el host se conecta o se
  cae, para enterarte de las caídas sin mirar la ventana.
- **Arranque con la sesión**, timeouts, frecuencia de petición y método de ping configurables.
- **Recuerda tus ajustes** entre ejecuciones.

## Descarga

Consigue el instalador de Windows (`Pingmaster-*-windows-x64-setup.exe`) o el paquete para tu Linux en
los [releases](https://github.com/blacknoize404/Pingmaster/releases):

| Distribución | Paquete |
|---|---|
| Windows 10/11 (x64) | `Pingmaster-*-windows-x64-setup.exe` (Inno Setup, instalación por usuario) |
| Debian, Ubuntu y derivadas | `pingmaster_*.deb` (`sudo apt install ./pingmaster_*.deb`) |
| Fedora, openSUSE | `pingmaster-*.rpm` (`sudo dnf install ./pingmaster-*.rpm`) |
| Cualquier otra | `pingmaster-*.tar.gz`, con un `install.sh` que lo instala para tu usuario sin permisos de administrador |

Cada paquete trae su propio runtime de Java: no hace falta tener Java instalado.

La interfaz está en español.

## Código fuente

Los paquetes se construyen desde el repositorio privado `Pingmaster-src` con la misma cadena que
[MathUtils Studio](https://github.com/blacknoize404/MathUtils-Studio): Maven → ProGuard → jlink →
jpackage → Inno Setup / deb / rpm. Las librerías que usa son públicas:

- [NetworkUtils](https://github.com/blacknoize404/NetworkUtils) — latencia de host y monitorización de tráfico de red (Apache-2.0)
- [PersistenceUtils](https://github.com/blacknoize404/PersistenceUtils) — ajustes en fichero (Apache-2.0)

## Licencias

Pingmaster en sí es propietario y de uso gratuito: mira [LICENSE](LICENSE) y [NOTICE.md](NOTICE.md)
para los componentes de terceros que llevan los instaladores.
