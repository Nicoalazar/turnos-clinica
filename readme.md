# Turnos Clínica Médica

Demo: https://nicoalazar.github.io/cursoJS-Flex/

Aplicación web para reservar citas médicas en una clínica online.

## Características
- Buscar doctores por especialidad y cobertura médica.
- Ver disponibilidad de doctores.
- Reservar citas con doctores disponibles.
- Ver historial de citas.

## Requisitos
- Navegador moderno.
- Servidor HTTP local (necesario para que `fetch` cargue `data.json`).

## Instalación y ejecución
1. Clona el repositorio.
2. Inicia un servidor local en la raíz del proyecto:

   ```bash
   python3 -m http.server 8000
   ```

3. Abre `http://localhost:8000` en tu navegador.

## Uso

### Búsqueda de doctores
1. Selecciona una especialidad del menú desplegable.
2. Indica si tienes cobertura médica.
3. Haz clic en **Buscar Médicos**.

### Reservar una cita
1. Si hay doctores disponibles y no tienes cobertura médica, el listado mostrará todos los doctores disponibles.
2. Si hay doctores disponibles y tienes cobertura médica, el listado mostrará solo los doctores que reciben cobertura médica.
3. Si el doctor no está disponible, se mostrará su nombre con un mensaje informativo.
4. Si el doctor está disponible, selecciona una fecha para la cita.
5. Haz clic en **Reservar**.

### Ver historial de citas
El historial de citas se muestra en la sección **Historial de Citas** después de reservar una cita.

## Estructura del proyecto
- `index.html`: estructura principal de la aplicación.
- `styles.css`: estilos base.
- `appointments.js`: lógica de búsqueda y reserva de citas.
- `data.json`: datos de doctores disponibles.

## Mejoras sugeridas
- Agregar autenticación para registrar al paciente real en la reserva.
- Persistir el historial de citas en `localStorage` o una API para conservarlo al recargar.
- Validar horario (hora) además de la fecha para evitar reservas ambiguas.
- Agregar tests básicos de lógica (filtros y reservas).

## Contribución
1. Haz un fork del proyecto.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Haz commit de tus cambios (`git commit -am 'Agrega nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Crea un Pull Request.
