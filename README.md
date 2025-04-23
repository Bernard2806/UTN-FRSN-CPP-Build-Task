<img align="right" width="200" height="100" src="https://github.com/user-attachments/assets/a0827ca6-20b7-4532-83b0-dd918cbcbc4d">

### Tarea de Compilación C/C++ - UTN FRSN - Aula Chivilcoy  
###### Universidad Tecnológica Nacional - Facultad Regional San Nicolás (UTN FRSN)  
###### Tecnicatura Universitaria en Programación - 2025  

---

> ***Este repositorio contiene una tarea de compilación reutilizable para proyectos en C/C++, pensada para facilitar el desarrollo de prácticas y trabajos durante el cursado de la Tecnicatura en Programación en la UTN FRSN.***

---

### 🧰 Cómo instalar el compilador de C/C++ (MSYS2 + MinGW-w64)

1. **Descargar e instalar MSYS2**  
   - Descargá el instalador desde la [página oficial de MSYS2](https://www.msys2.org) o directamente desde este [enlace](https://github.com/msys2/msys2-installer/releases/latest).  
   - Ejecutá el instalador y seguí los pasos. Requiere Windows 8.1 (64 bits) o superior.

2. **Configurar la instalación**  
   - Elegí una carpeta de instalación (por defecto: `C:\msys64`) y finalizá la instalación con la opción **"Run MSYS2 now"** activada.

3. **Instalar el toolchain de MinGW-w64**  
   - En la terminal que se abre, ejecutá:

   ```bash
   pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain
   ```

   - Presioná **Enter** para aceptar la instalación de los paquetes. Cuando se te pregunte, escribí `Y` y presioná **Enter**.

4. **Agregar MinGW-w64 al PATH del sistema**

   - Abrí el menú de inicio y buscá **"Editar variables de entorno"**.
   - En *Variables de usuario*, seleccioná `Path` y hacé clic en **Editar**.
   - Agregá una nueva entrada con la ruta (por defecto):

     ```
     C:\msys64\ucrt64\bin
     ```

   - Guardá los cambios con **Aceptar**.

   > 💡 Cerrá y volvé a abrir las consolas para aplicar el nuevo `PATH`.

5. **Verificar la instalación**

   - En una nueva terminal, ejecutá:

   ```bash
   gcc --version
   g++ --version
   gdb --version
   ```

   - Si todo está correcto, deberías ver las versiones instaladas. Si no:

    - Asegurate de que la ruta agregada al `PATH` sea correcta.
    - Si `gdb` no funciona, ejecutá:

     ```bash
     pacman -S mingw-w64-ucrt-x86_64-gdb
     ```

---
