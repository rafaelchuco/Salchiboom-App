
# [🍔SalchiBoom🍔](https://www.figma.com/proto/mM4dnzuRfXycxZJnjydGVo/Mapa?node-id=45-95&node-type=frame&t=W6D1BGtgHvrUYwic-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=55%3A95)
![SalchiBoom](./imagenes-logo/SalchiboomPantalla.png)

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
      - [Productos](#productos)
      - [Categoria](#categoria)
      - [Pedidos](#pedidos)
      - [Carrito](#carrito)
      - [Metodo\_Pago](#metodo_pago)
      - [Historial\_Pago](#historial_pago)
      - [Reseña\_Producto](#reseña_producto)
      - [Direccion\_Envio](#direccion_envio)
      - [Historial\_Pedido](#historial_pedido)
      - [Cupones](#cupones)
      - [Restaurantes](#restaurantes)
      - [Inventario](#inventario)
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
| Teléfono          | Varchar(25)   |
| Dirección         |  Text         |

#### Repartidores
| Attribute         | Type          |
| ----------------- | ------------- |
| Id_repartidor     |     INT       |
| id_usuario        |     INT       |
| estatus           |     Enum      |

#### Productos
| Attribute         | Type          |
| ----------------- | ------------- |
| id_producto       | INT           |
| Nombre            | Varchar(10)   |
| Precio            | Decimal(10, 2)|
| Descripción       | Text          |
| id_categoria      | INT           |

#### Categoria
| Attribute         | Type          |
| ----------------- | ------------- |
| id_categoria      | INT           |
| Nombre            |  Charchar(25) |

#### Pedidos
| Attribute         | Type          |
| ----------------- | ------------- |
| id_pedido         |     INT       |
| id_usuario        |     INT       |
| fecha_pedido      |     Date      |
| total             |  Decimal      |

#### Carrito
| Attribute         | Type          |
| ----------------- | ------------- |
| id_carrito        |     INT       |
| id_usuario        |     INT       |
| id_producto       |     INT       |
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
| id_pedido         |    INT        |
| id_metodo_pago    |    INT        |
| fecha_pago        |    Date       |

#### Reseña_Producto
| Attribute         | Type          |
| ----------------- | ------------- |
| id_reseña         |     INT       |
| id_producto       |     INT       |
| id_usuario        |     INT       |
| comentario        |     Text      |
| Calificacion      |     INT       |

#### Direccion_Envio
| Attribute         | Type          |
| ----------------- | ------------- |
| id_direccion      |  INT          |
| id_usuario        |  INT          |
| direccion         |  Varchar(25)  |
| ciudad            |  Varchar(15)  |
| estado            |  Varchar(15)  |


#### Historial_Pedido
| Attribute         | Type          |
| ----------------- | ------------- |
| id_historial      |    INT        |
| id_pedido         |    INT        |
| estatus           |    INT        |

#### Cupones
| Attribute         | Type          |
| ----------------- | ------------- |
| id_usuario        |  INT          |
| Nombre            | Varchar(25)   |
| Email             | Varchar(25)   |
| Teléfono          | Varchar(25)   |
| Dirección         |  Text         |

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
| id_producto       |     INT       |
| Cantidad          |     INT       |

## Relaciones entre tablas

- **Usuarios** esta relacionada con:

- **Repartidores** esta relacionada con:

- **Productos** esta relacionada con:

- **Categoria** esta relacionada con:

- **Pedidos** esta relacionada con:

- **Carrito** esta relacionada con:

- **Metodo_Pago** esta relacionada con:

- **Historial_Pago** esta relacionada con:

- **Reseña_Producto** esta relacionada con:

- **Direccion_Envio** esta relacionada con:

- **Historial_Pedido** esta relacionada con:

- **Cupones** esta relacionada con:

- **Restaurantes** esta relacionada con:

- **Inventario** esta relacionada con:

## Diagrama Entidad-Relación
