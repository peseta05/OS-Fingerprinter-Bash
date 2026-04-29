# 🧙‍♂️ witchsystem

Es una herramienta de reconocimiento pasivo escrita en Bash que permite adivinar el sistema operativo de un host remoto analizando la respuesta de los paquetes ICMP.

## ✨ ¿Cómo funciona?
El script detecta la "firma" del valor **TTL (Time To Live)** para clasificar el objetivo:
*   **TTL ≤ 64:** Linux / macOS
*   **TTL ≤ 128:** Windows
*   **TTL > 128:** Dispositivos de Red (Cisco, Solaris, etc.) o sistemas Unix antiguo.

## 🚀 Instalación y Uso

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/peseta05/OS-Fingerprinter-Bash.git
   cd OS-Fingerprinter-Bash
   ```

2. **Dar permisos de ejecución:**
   ```bash
   chmod +x witchsystem
   ```

3. **Ejecutar:**
   ```bash
   ./witchsystem Ip_Objetivo
   ```

Si quieres usar **witchsystem** desde cualquier parte de tu terminal, sigue estos pasos:

1. **Mueve el archivo a /usr/local/bin con el nombre final**
```bash
sudo cp witchsystem /usr/local/bin/witchsystem
```

2. **Asegúrate de que tenga permisos de ejecución**
```bash
sudo chmod +x /usr/local/bin/witchsystem
```

3. **¡Listo! Ahora solo escribe el comando seguido de la IP**
```bash
witchsystem Ip_Objetivo
```

## 🛠️ Requisitos
*   Bash
*   Utilidad `ping`
*   Grep (con soporte Perl-RegEx `-P`)

---
Desarrollado con fines educativos y de auditoría de seguridad.
