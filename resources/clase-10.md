# Clase 10 

## Temas
- Clientes http: Axios / Fetch
- MockServer: Json server
- Resilencia: Status codes 
- Renderizado condicional: UseEffect

### 1 - Levantando el mock server - Json server

Pasos para instalar y correr json server en nuestro proyecto front end.

1. `npm install json-server --save-dev`
2. Crear `db.json` en `./test/resources`
```json
{
  "users": [
    {
      "id": 1,
      "nombre": "Juan",
      "apellido": "Pérez",
      "estado": "nuevo",
      "fechaCreacion": "2023-10-10"
    },
    {
      "id": 2,
      "nombre": "Ana",
      "apellido": "Gómez",
      "estado": "pendiente",
      "fechaCreacion": "2023-10-08"
    }
  ]
}
```
3. Correr el json server `npx json-server --watch ./test/resources/db.json --port 3001`
4. (opcional) agregar el comando para correr con npm run. En `package.json`, dentro de **scripts** definir el server asi: `"json-server": "json-server --watch db.json --port 3001"`
5. (opcional) Se puede correr el json server: `npm run json-server`

### 2 - Interactuando con el servidor mediante axios

1. Instalar axios `npm install axios`
2. 
Crear una pantalla que permita hacer las siguientes interacciones

Siguientes interacciones:
- Crear un usuario con: nombre, apellido, estado [nuevo, pendiente, bloqueado], fecha de creacion.
- Ver lista de usuarios
- Ver lista de usuarios segun nombre
- Modificar estado de usuario
- Eliminar usuario

### 3 - Status code

Cada interaccion anterior debe proveer un mensaje de 500

### 4 - Renderizado condicional

Mostrar el nombre de usuario con algun color segun el estado