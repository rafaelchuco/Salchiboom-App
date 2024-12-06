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



