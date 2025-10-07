# Product Catalog API

API y aplicación de interfaz de usuario para un catálogo de productos.  
Esta herramienta permite:

- **Usuarios**: autenticarse y consultar productos.
- **Administradores**: control total sobre las operaciones CRUD de los productos.

---

## Reglas de negocio

- Autenticación obligatoria para usuarios.
- Los productos pueden ser agregados, visualizados, modificados o eliminados.
- Los productos pueden buscarse y filtrarse por **nombre** y **precio**.
- La información de productos se consume desde la API externa **DummyJSON**.
- Solo los administradores pueden realizar operaciones CRUD completas.
- Los usuarios autenticados pueden ver y buscar productos.

---

## Tecnologías utilizadas

- **Backend**: Node.js con NestJS (Framework recomendado por su estructura modular y soporte para escalabilidad).
- **Autenticación**: JWT.
- **Frontend**: React (Angular también considerado opcionalmente).
- **Control de versiones**: Git con commits frecuentes.
- **Documentación**: Este archivo README.md y comentarios en el código.

**Opcionales / Puntos extras:**

- Uso de **GraphQL** para consultas y mutaciones.
- Contenerización mediante **Docker**.
- Incorporación de otras tecnologías o mejoras que aporten valor al proyecto.

---

## Endpoints principales

### Autenticación

- `POST /auth/login` → Iniciar sesión y recibir un token JWT.

### Productos

- `GET /products` → Obtener todos los productos (usuarios autenticados).
- `GET /products?name=xxx&price=xxx` → Filtrar productos por nombre y precio.
- `POST /products` → Crear un producto (solo administradores).
- `PUT /products/:id` → Editar un producto existente (solo administradores).
- `DELETE /products/:id` → Eliminar un producto (solo administradores).

---

## Instalación

1. Clonar el repositorio:

```bash
git clone https://github.com/ChuckmonsterXlx/product-catalog-api.git
cd product-catalog-api
```
