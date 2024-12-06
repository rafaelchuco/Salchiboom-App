# [🍔SalchiBoom🍔](https://www.figma.com/proto/mM4dnzuRfXycxZJnjydGVo/Mapa?node-id=45-95&node-type=frame&t=W6D1BGtgHvrUYwic-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=55%3A95)
![SalchiBoom](./img-logo/SalchiboomPantalla.png)

### Tabla de contenido
- [🍔SalchiBoom🍔](#salchiboom)
    - [Tabla de contenido](#tabla-de-contenido)
  - [Objetivos](#objetivos)
    - [Objetivo general](#objetivo-general)
    - [Objetivos específicos](#objetivos-específicos)
  - [👨‍💻Tecnologías utilizadas](#tecnologías-utilizadas)
  - [Tablas y Atributos](#tablas-y-atributos)
      - [Usuarios](#usuarios)
      - [Repartidores](#repartidores)
      - [Restaurantes\_has\_Productos](#restaurantes_has_productos)
      - [Productos](#productos)
      - [Pedidos\_has\_usuarios](#pedidos_has_usuarios)
      - [Pedidos](#pedidos)
      - [Carrito](#carrito)
      - [Metodo\_Pago](#metodo_pago)
      - [Historial\_Pago](#historial_pago)
      - [Reseña\_Producto](#reseña_producto)
      - [Direccion\_Envio](#direccion_envio)
      - [Especificación\_Producto](#especificación_producto)
      - [Cupones](#cupones)
      - [Restaurantes](#restaurantes)
      - [Inventario](#inventario)
      - [Especificaciones](#especificaciones)
      - [Registro](#registro)
  - [Relaciones entre tablas](#relaciones-entre-tablas)
  - [Diagrama Entidad-Relación](#diagrama-entidad-relación)
  - [Script](#script)

## Objetivos
### Objetivo general
Desarrollar una aplicación móvil que permita a los usuarios realizar pedidos de comida rápida de manera eficiente, con una experiencia de usuario optimizada que permita la programación de pedidos y el seguimiento en tiempo real.
### Objetivos específicos
- Ofrecer una interfaz de usuario intuitiva y de fácil acceso para usuarios de diferentes edades y niveles de conocimiento tecnológico.
  
- Integrar un sistema de pago en línea seguro, rápido y versátil para facilitar las transacciones.
  
- Implementar un sistema de seguimiento en tiempo real de los pedidos, desde su preparación hasta la entrega.
## 👨‍💻Tecnologías utilizadas
<table>
  <thead>
    <tr>
      <th>Figma</th>
      <th>Oracle</th>
      <th>MySQL Workbench</th>
      <th>Google Docs</th>
    </tr>
  </thead>
  <tbody>
    <td>
        <img src="https://www.kindpng.com/picc/m/81-814934_figma-logo-png-transparent-png.png"width="100%" />
    </td>
    <td>
        <img src="https://m.media-amazon.com/images/I/41QodfboFdL.png"width="100%" />
    </td>
    <td>
        <img src="https://wizcase.com/wp-content/uploads/2022/02/MySQL-Workbench-logo.png"width="100%" />
    </td>
    <td>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/66/Google_Docs_2020_Logo.svg/1489px-Google_Docs_2020_Logo.svg.png"width="100%"/>
    </td>
  </tbody>
</table>

## Tablas y Atributos

#### Usuarios

| Attribute         | Type          |
| ----------------- | ------------- |
| id_usuario        |  INT          |
| Nombre            | Varchar(25)   |
| Email             | Varchar(25)   |
| Dirección         |  Text         |
| Teléfono          | Varchar(25)   |

#### Repartidores

| Attribute         | Type          |
| ----------------- | ------------- |
| Id_repartidor     |     INT       |
| estatus           |     Enum      |

#### Restaurantes_has_Productos

| Attribute         | Type          |
| ----------------- | ------------- |
|id_categoria       |  Varchar(45)  |
|Nombre             |  Varchar(45)  |

#### Productos

| Attribute         | Type          |
| ----------------- | ------------- |
| id_producto       | INT           |
| Nombre            | Varchar(10)   |
| Precio            | Decimal(10, 2)|
| Descripción       | Text          |

#### Pedidos_has_usuarios

| Attribute         | Type          |
| ----------------- | ------------- |
| id_historial      | INT           |

#### Pedidos

| Attribute         | Type          |
| ----------------- | ------------- |
| id_pedido         |     INT       |
| fecha_pedido      |     Date      |
| total             |  Decimal      |

#### Carrito

| Attribute         | Type          |
| ----------------- | ------------- |
| id_carrito        |     INT       |
| Cantidad          |     INT       |

#### Metodo_Pago

| Attribute         | Type          |
| ----------------- | ------------- |
| Id_método_pago    |      INT      |
| Nombre            | Varchar(25)  |

#### Historial_Pago

| Attribute         | Type          |
| ----------------- | ------------- |
| id_pago           |    INT        |
| fecha_pago        |    Date       |

#### Reseña_Producto

| Attribute         | Type          |
| ----------------- | ------------- |
| id_reseña         |     INT       |
| comentario        |     Text      |
| Calificacion      |     INT       |

#### Direccion_Envio

| Attribute         | Type          |
| ----------------- | ------------- |
| id_direccion      |  INT          |
| direccion         |  Varchar(25)  |
| ciudad            |  Varchar(15)  |
| estado            |  Varchar(15)  |


#### Especificación_Producto

| Attribute         | Type          |
| ----------------- | ------------- |
| valor             |Varchar(45)    |

#### Cupones

| Attribute         | Type          |
| ----------------- | ------------- |
| id_cupon          |  INT          |
| codigo            | Varchar(25)   |
| descuento         | Varchar(25)   |
| fecha_vencimiento | Varchar(25)   |

#### Restaurantes

| Attribute         | Type          |
| ----------------- | ------------- |
|  id_restaurante   |  INT          |
|  Nombre           |  Varchar(10)  |
|  Descripción      |  clob         |

#### Inventario

| Attribute         | Type          |
| ----------------- | ------------- |
| id_inventario     |     INT       |
| Cantidad          |     INT       |

#### Especificaciones

| Attribute         | Type          |
| ----------------- | ------------- |
| id_especificacion |     INT       |
| Nombre            |     INT       |
| Descripción       |     INT       |

#### Registro

| Attribute         | Type          |
| ----------------- | ------------- |
| id_registro       |     INT       |
| id_usuario        |     INT       |
| correo            |  Varchar(25)  |
| contraseña        |  Varchar(25)  |
| direccion         |  Varchar(45)  |
| telefono          |  Varchar(15)  |
| Nombre            |  Varchar(25)  |



## Relaciones entre tablas

- **Usuarios** esta relacionada con:
  -Carrito
  - Direccion_Envio
  - Cupones
  - Repartidores
  - Registro
  - Reseña_Producto
  - Pedidos_has_usuarios

- **Repartidores** esta relacionada con:
  - Usuarios

- **Productos** esta relacionada con:
  - Reseña_producto
  - Especificación_Producto
  - Inventario
  - Carrito
  - Categoria

- **Pedidos** esta relacionada con:
  - Historial_Pago
  - Historial_pedidos

- **Carrito** esta relacionada con:
  - Productos
  - Usuarios

- **Metodo_Pago** esta relacionada con:
  - Historial_Pago

- **Historial_Pago** esta relacionada con:
  - Pedidos
  - Historial_Pedidos

- **Reseña_Producto** esta relacionada con:
  - Productos
  - Usuarios

- **Direccion_Envio** esta relacionada con:
  - Usuarios

- **Categorías** esta relacionada con:
  - Restaurantes
  - Productos 

- **Cupones** esta relacionada con:
  - Usuarios

- **Restaurantes** esta relacionada con:
  - Categoria

- **Inventario** esta relacionada con:
  - Productos

## Diagrama Entidad-Relación

![der](./img-logo/der_SB.jpg)

## Script

```sql
-- Tabla Categoria
CREATE TABLE salchiboom.Categoria (
  id_categoria NUMBER GENERATED ALWAYS AS IDENTITY,
  nombre_categoria VARCHAR2(100) NOT NULL,
  CONSTRAINT pk_categoria PRIMARY KEY (id_categoria)
);

-- Tabla Productos
CREATE TABLE salchiboom.Productos (
  id_producto NUMBER GENERATED ALWAYS AS IDENTITY,
  nombre_producto VARCHAR2(100) NOT NULL,
  precio NUMBER(10,2) NOT NULL,
  descripcion CLOB,
  id_categoria NUMBER NOT NULL,
  stock NUMBER,
  valoracion NUMBER(2,1),
  CONSTRAINT pk_productos PRIMARY KEY (id_producto),
  CONSTRAINT fk_productos_categoria FOREIGN KEY (id_categoria)
    REFERENCES salchiboom.Categoria (id_categoria)
    ON DELETE CASCADE
);

-- Tabla Usuarios
CREATE TABLE salchiboom.Usuarios (
  id_usuario NUMBER GENERATED ALWAYS AS IDENTITY,
  nombre VARCHAR2(100) NOT NULL,
  email VARCHAR2(100) NOT NULL,
  direccion VARCHAR2(255) NOT NULL,
  telefono VARCHAR2(15) NOT NULL,
  Registro_idRegistro NUMBER NOT NULL,
  Registro_IdUsuario NUMBER NOT NULL,
  CONSTRAINT uq_usuarios_email UNIQUE (email),
  CONSTRAINT pk_usuarios PRIMARY KEY (id_usuario, Registro_idRegistro, Registro_IdUsuario),
  CONSTRAINT fk_Usuarios_Registro1 FOREIGN KEY (Registro_idRegistro, Registro_IdUsuario)
    REFERENCES mydb.Registro (idRegistro, IdUsuario)
);

-- Tabla Repartidores (ENUM a CHECK)
CREATE TABLE salchiboom.Repartidores (
  id_repartidor NUMBER GENERATED ALWAYS AS IDENTITY,
  id_usuario NUMBER NOT NULL,
  estatus VARCHAR2(10) NOT NULL,
  CONSTRAINT pk_repartidores PRIMARY KEY (id_repartidor),
  CONSTRAINT ck_repartidores_estatus CHECK (estatus IN ('activo', 'inactivo')),
  CONSTRAINT fk_repartidores_usuarios FOREIGN KEY (id_usuario)
    REFERENCES salchiboom.Usuarios (id_usuario)
    ON DELETE CASCADE
);

-- Tabla Pedidos
CREATE TABLE salchiboom.Pedidos (
  id_pedido NUMBER GENERATED ALWAYS AS IDENTITY,
  fecha_pedido TIMESTAMP NOT NULL,
  total NUMBER(10,2) NOT NULL,
  CONSTRAINT pk_pedidos PRIMARY KEY (id_pedido)
);

-- Tabla Carrito
CREATE TABLE salchiboom.Carrito (
  id_carrito NUMBER GENERATED ALWAYS AS IDENTITY,
  id_usuario NUMBER NOT NULL,
  id_producto NUMBER NOT NULL,
  cantidad NUMBER NOT NULL,
  CONSTRAINT pk_carrito PRIMARY KEY (id_carrito),
  CONSTRAINT fk_carrito_usuarios FOREIGN KEY (id_usuario)
    REFERENCES salchiboom.Usuarios (id_usuario),
  CONSTRAINT fk_carrito_productos FOREIGN KEY (id_producto)
    REFERENCES salchiboom.Productos (id_producto)
);

-- Tabla Metodo_Pago
CREATE TABLE salchiboom.Metodo_Pago (
  id_metodo_pago NUMBER GENERATED ALWAYS AS IDENTITY,
  nombre_metodo VARCHAR2(50) NOT NULL,
  CONSTRAINT pk_metodo_pago PRIMARY KEY (id_metodo_pago)
);

-- Tabla Historial_Pago
CREATE TABLE salchiboom.Historial_Pago (
  id_pago NUMBER GENERATED ALWAYS AS IDENTITY,
  id_pedido NUMBER NOT NULL,
  id_metodo_pago NUMBER NOT NULL,
  fecha_pago TIMESTAMP NOT NULL,
  CONSTRAINT pk_historial_pago PRIMARY KEY (id_pago),
  CONSTRAINT fk_historial_pago_pedidos FOREIGN KEY (id_pedido)
    REFERENCES salchiboom.Pedidos (id_pedido),
  CONSTRAINT fk_historial_pago_metodo FOREIGN KEY (id_metodo_pago)
    REFERENCES salchiboom.Metodo_Pago (id_metodo_pago)
);

-- Tabla Reseña_Producto
CREATE TABLE salchiboom."Reseña_Producto" (
  id_reseña NUMBER GENERATED ALWAYS AS IDENTITY,
  id_producto NUMBER NOT NULL,
  id_usuario NUMBER NOT NULL,
  comentario CLOB NOT NULL,
  calificación NUMBER NOT NULL,
  CONSTRAINT pk_reseña_producto PRIMARY KEY (id_reseña),
  CONSTRAINT fk_reseña_producto_productos FOREIGN KEY (id_producto)
    REFERENCES salchiboom.Productos (id_producto),
  CONSTRAINT fk_reseña_producto_usuarios FOREIGN KEY (id_usuario)
    REFERENCES salchiboom.Usuarios (id_usuario)
);

-- Tabla Direccion_Envio
CREATE TABLE salchiboom.Direccion_Envio (
  id_direccion NUMBER GENERATED ALWAYS AS IDENTITY,
  id_usuario NUMBER NOT NULL,
  direccion VARCHAR2(255) NOT NULL,
  ciudad VARCHAR2(100) NOT NULL,
  estado VARCHAR2(100) NOT NULL,
  CONSTRAINT pk_direccion_envio PRIMARY KEY (id_direccion),
  CONSTRAINT fk_direccion_envio_usuarios FOREIGN KEY (id_usuario)
    REFERENCES salchiboom.Usuarios (id_usuario)
);

-- Tabla Historial_Pedido (ENUM a CHECK)
CREATE TABLE salchiboom.Historial_Pedido (
  id_historial NUMBER GENERATED ALWAYS AS IDENTITY,
  id_pedido NUMBER NOT NULL,
  estatus VARCHAR2(20) NOT NULL,
  CONSTRAINT pk_historial_pedido PRIMARY KEY (id_historial),
  CONSTRAINT ck_historial_pedido_estatus CHECK (estatus IN ('en preparación', 'en camino', 'entregado', 'cancelado')),
  CONSTRAINT fk_historial_pedido_pedidos FOREIGN KEY (id_pedido)
    REFERENCES salchiboom.Pedidos (id_pedido)
);

-- Tabla Cupones
CREATE TABLE salchiboom.Cupones (
  id_cupon NUMBER GENERATED ALWAYS AS IDENTITY,
  codigo VARCHAR2(50) NOT NULL,
  descuento NUMBER(5,2) NOT NULL,
  fecha_vencimiento DATE NOT NULL,
  Usuarios_id_usuario NUMBER NOT NULL,
  CONSTRAINT pk_cupones PRIMARY KEY (id_cupon, Usuarios_id_usuario),
  CONSTRAINT fk_Cupones_Usuarios1 FOREIGN KEY (Usuarios_id_usuario)
    REFERENCES salchiboom.Usuarios (id_usuario)
);

-- Tabla Restaurantes
CREATE TABLE salchiboom.Restaurantes (
  id_restaurante NUMBER GENERATED ALWAYS AS IDENTITY,
  nombre VARCHAR2(100) NOT NULL,
  "Horario_atención" CLOB,
  CONSTRAINT pk_restaurantes PRIMARY KEY (id_restaurante)
);

-- Tabla Inventario
CREATE TABLE salchiboom.Inventario (
  id_inventario NUMBER GENERATED ALWAYS AS IDENTITY,
  id_producto NUMBER NOT NULL,
  cantidad_disponible NUMBER NOT NULL,
  CONSTRAINT pk_inventario PRIMARY KEY (id_inventario),
  CONSTRAINT fk_inventario_productos FOREIGN KEY (id_producto)
    REFERENCES salchiboom.Productos (id_producto)
);

-- Tabla Pedidos_has_Usuarios
CREATE TABLE salchiboom.Pedidos_has_Usuarios (
  Pedidos_id_pedido NUMBER NOT NULL,
  Usuarios_id_usuario NUMBER NOT NULL,
  id_historial NUMBER,
  CONSTRAINT pk_pedidos_has_usuarios PRIMARY KEY (Pedidos_id_pedido, Usuarios_id_usuario),
  CONSTRAINT fk_Pedidos_has_Usuarios_Pedidos1 FOREIGN KEY (Pedidos_id_pedido)
    REFERENCES salchiboom.Pedidos (id_pedido),
  CONSTRAINT fk_Pedidos_has_Usuarios_Usuarios1 FOREIGN KEY (Usuarios_id_usuario)
    REFERENCES salchiboom.Usuarios (id_usuario)
);

-- Tabla Restaurantes_has_Productos
CREATE TABLE salchiboom.Restaurantes_has_Productos (
  Restaurantes_id_restaurante NUMBER NOT NULL,
  Productos_id_producto NUMBER NOT NULL,
  id_categoria VARCHAR2(45) NOT NULL,
  Nombre VARCHAR2(45),
  CONSTRAINT pk_restaurantes_has_productos PRIMARY KEY (Restaurantes_id_restaurante, Productos_id_producto, id_categoria),
  CONSTRAINT uq_rhp_id_categoria UNIQUE (id_categoria),
  CONSTRAINT uq_rhp_productos_id_producto UNIQUE (Productos_id_producto),
  CONSTRAINT uq_rhp_restaurantes_id_restaurante UNIQUE (Restaurantes_id_restaurante),
  CONSTRAINT fk_Restaurantes_has_Productos_Restaurantes1 FOREIGN KEY (Restaurantes_id_restaurante)
    REFERENCES salchiboom.Restaurantes (id_restaurante),
  CONSTRAINT fk_Restaurantes_has_Productos_Productos1 FOREIGN KEY (Productos_id_producto)
    REFERENCES salchiboom.Productos (id_producto)
);
```
