# 🧙‍♂️ witchsystem

**witchsystem** es una herramienta de reconocimiento pasivo escrita en Bash que permite adivinar el sistema operativo de un host remoto analizando la respuesta de los paquetes ICMP.

## ✨ ¿Cómo funciona?
El script detecta la "firma" del valor **TTL (Time To Live)** para clasificar el objetivo:
*   **TTL ≤ 64:** Linux / macOS
*   **TTL ≤ 128:** Windows
*   **TTL > 128:** Dispositivos de Red (Cisco, Solaris, etc.)

## 🚀 Instalación y Uso

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com
   cd witchsystem
   ```

2. **Dar permisos de ejecución:**
   ```bash
   chmod +x witchsystem.sh
   ```

3. **Ejecutar:**
   ```bash
   ./witchsystem.sh 192.168.1.1
   ```

## 🛠️ Requisitos
*   Bash
*   Utilidad `ping`
*   Grep (con soporte Perl-RegEx `-P`)

---
Desarrollado con fines educativos y de auditoría de seguridad.
