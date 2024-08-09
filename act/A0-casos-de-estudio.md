# Casos de Estudio

1. [Caso ONG: Médicos sin Frontera](#caso-ong-médicos-sin-frontera)
1. [Caso Reserva Ecológica](#caso-reserva-ecológica)
1. [Caso YouTube Lite](#caso-youtube-lite)
1. [Caso Registro de las Personas de la Pcia. de Bs. As.](#caso-registro-de-las-personas-de-la-pcia-de-buenos-aires)
1. [Caso Distribuidora de Productos Alimenticios](#caso-distribuidora-de-productos-alimenticios)
1. [Caso Tu Cine](#caso-tu-cine)
1. [Caso Web de la NBA](#caso-web-de-la-nba)
1. [Caso Gimnasio Red Hot Arms](#caso-gimnasio-red-hot-arms)
1. [Caso Twitter](#caso-twitter)
1. [Caso Bar Ghins](#caso-bar-ghins)
1. [Caso Negocios de Venta de Ropa](#caso-negocios-de-venta-de-ropa)
1. [Caso Spotify](#caso-spotify)

## Caso ONG: Médicos sin Frontera

La ONG “Médicos sin Fronteras”  tiene que manejar la información sobre las tareas que llevan a cabo sus voluntarios en las distintas zonas de conflicto distribuídas en diferentes lugares a lo largo del mundo.
Se nos solicita que diseñemos la base de datos para el sistema informático de la ONG, para locual se tienen las siguientes reglas de negocio (documento de requisitos):

1. De cada tarea se sabe: el nombre (que puede repetirse entre las distintas tareas), el código de la tarea (que es único para cada tarea), cuántas horas por semana conviene dedicarle como mínimo, cuantas horas por semana se le puede dedicar como máximo, una fecha de inicio, una fecha de fin (si es que está finalizada) y el presupuesto asignado a la misma.
2. De los lugares donde se hacen tareas se debe manejar: un nombre que se puede repetir, sus coordenadas (latitud y longitud), que identifican al lugar, su medio de acceso (auto, 4x4, camión, avión, barco, tren), sus paradas para alojamiento (que pueden no tener)  y el país en donde está ubicado.
3. De cada alojamiento se almacena un código, que se repite dentro del lugar al que pertenecen y una dirección que está conformada por calle, número, ciudad, código postal, piso y depto, los dos últimos datos pueden no corresponder a una dirección.
4. Puede pasar que distintas tareas se hagan en el mismo lugar, pero no sucede que una misma tarea se realice en varios lugares. De hecho, cada tarea se realiza en un solo lugar.
5. De cada país se conoce su nombre que es único, el continente en que está ubicado (ASIA, AMÉRICA DEL SUR, AMÉRICA CENTRAL, AMÉRICA DEL NORTE, ÁFRICA, ANTÁRTIDA, EUROPA, OCEANÍA) y el grado de conflictividad (de algunos países no se tiene esta información), que es un número entero del 1 al 10 (1: todo tranquilo, 10: guerra civil, etc.).
6. En los países se hablan distintos idiomas y cada idioma se habla al menos en un país. Cada país tiene como mínimo un idioma oficial, se quieren saber tanto los idiomas oficiales como los no oficiales.
7. De los idiomas se tiene un código alfanumérico único y el nombre, que también es único.
8. De cada voluntario de la ONG se sabe: nombre, apellido, email, teléfonos, DNI, que se puede repetir,  país en donde vive y los idiomas que habla. Se toma como supuesto semántico que no puede haber dos personas que compartan su email, ya que es una forma de comunicarse con los voluntarios por parte de la ONG.
9. Los voluntarios pueden ser médicos o personas civiles que se alistan en la ONG para prestar distintos servicios. De los médicos se conoce su especialidad, la matrícula que es única y los años de antigüedad que hace que ejerce como tal. De las personas civiles se tiene una descripción de la actividad que puede aportar a la ONG. Por ejemplo, ayuda en tareas de enfermería, cocina, conduce autos y helicópteros, etc.
10. De cada especialidad se tiene un código y un nombre. Ambos datos deben ser únicos.
11. De algunos voluntarios se desconoce el país donde viven.
12. Cada voluntario trabaja en una o en muchas tareas, para cada una de ellas se sabe cuántas horas le dedica por semana. En una tarea pueden trabajar varios voluntarios.
13. Se quiere saber el período de tiempo que un voluntario trabaja en una tarea, es decir, la  fecha de inicio y la fecha de fin (que puede no saberse). Además, se sabe que un voluntario puede rotar entre las distintas tareas en las que trabaja en distintos períodos de tiempo, pudiendo estar en una misma tarea más de un período.
14. Cada tarea puede tener (aunque no siempre) un coordinador, que es un voluntario, que puede o no trabajar en esa tarea. Un voluntario solo puede coordinar varias tareas.
15. Se quiere saber la cantidad total de horas semanales que trabaja un voluntario entre todas las tareas que realiza.
16. Algunos voluntarios son jefes de otro grupo de voluntarios.
17. En las tareas se usan insumos que se compran a distintos proveedores. Se quiere saber qué insumos son provistos por los proveedores en las tareas.
18. De los insumos se conoce el código, que es único, el nombre y se tiene una descripción.
19. De los proveedores se conoce el CUIT, que es único, la razón social, que es única que se puede repetir, el nombre comercial, que es único, el email que es único, la dirección y el teléfono.

## Caso Reserva Ecológica

Las autoridades de la Reserva Ecológica  se encuentran en un proceso de sistematización y necesitan diseñar una base de datos, para lo cual, se cuenta con los siguientes requisitos:

1. La Reserva Ecológica contará con varios empleados, a cada uno de estos le corresponderá un legajo, que es un dato alfanumérico y único, nombre, apellido, DNI, CUIL, números de teléfono, email (que es único), fecha de nacimiento, fecha de inicio de actividades, fecha de baja, la cual tendrá un valor sólo en el caso de que el empleado no forme más parte de la planta de la Reserva; y el salario. Los empleados a su vez pueden ser veterinarios, cuidadores o guías.
2. Cada veterinario tendrá su respectiva matrícula, que es única, su especialidad o especialidades y los años de experiencia que tenga.
3. La especialidad de los veterinarios podrá ser Cardiología, Oftalmología, Oncología, Ortopedia o Reproducción.
4. Un empleado podrá supervisar a ninguno o muchos empleados y cada empleado podrá ser supervisado como máximo por un único empleado.
5. Cada especie animal poseerá su correspondiente código alfanumérico de especie, una descripción breve, características, cantidad de animales que hay en la reserva de esa especie, nombre vulgar, nombre científico, peligro de extinción y grupo.
6. El grupo de las especies puede ser Mamíferos, Aves, Reptiles, Peces, Insectos o Arañas y Alacranes.
7. El peligro de extinción de las especies podrá ser Rojo, Amarillo o Verde, dependiendo del peligro de extinción que corra la misma.
8. Cada animal contará con su respectivo código alfanumérico de animal (que es único), peso, color, sexo, que toma los valores, macho o hembra; y una fecha de nacimiento estimada.
9. Un animal podrá pertenecer a una única especie y a cada especie pertenecerán muchos animales.
10. En la Reserva existen varios parques. Cada parque cuenta con su respectivo nombre, que es único, dirección, días que abre, hora de apertura y hora de cierre, que dependen del día. Por ejemplo, un día de semana cierra a las 18:00 y sábados y domingos a las 19:00. La dirección estará compuesta por la ciudad, calle, número y código postal.
11. Cada hábitat tendrá su debido código alfanumérico de hábitat que se repite dentro de cada parque, nombre, tipo, clima, vegetación y extensión (medida en hectáreas).
12. El tipo de cada hábitat puede ser Aviario, Acuario, Delfinario o Terrario.
13. El clima de cada hábitat puede ser Tropical, Seco, Templado, Continental o Polar.
14. La vegetación de cada hábitat puede ser Pantano, Lago, Rio, Mar, Tundra, Taiga, Selva, Bosque, Desierto o Sabana.
15. Un parque albergará muchos hábitats y un hábitat será albergado por un único parque.
16. Un empleado podrá trabajar en un único parque y en cada parque podrán trabajar muchos empleados.
17. Los veterinarios son los encargados de dar diagnósticos y tratamientos médicos a los animales de la Reserva. Cada tratamiento contará con un número único, un diagnóstico, una descripción (sobre medicamentos, alimentación, etc.), una sugerencia (que puede no estar) y la fecha en que fue realizado, sabiendo que un animal puede tener muchos tratamientos a lo largo del tiempo, pero cada tratamiento de un animal lo indica un solo veterinario.
18. Un cuidador podrá cuidar muchos hábitats y cada hábitat podrá ser cuidado por muchos cuidadores. Se quiere saber el período en los que cada cuidador cuida los distintos hábitats, ya que se asignan por distintos períodos de tiempo.
19. Un guía podrá recorrer muchos hábitats y cada hábitat podrá ser recorrido por muchos guías.
20. Un animal vivirá en un único hábitat y en cada hábitat podrán vivir muchos animales.

## Caso YouTube Lite

Intentaremos diseñar un modelo sencillo pensando en cómo sería la base de datos para una versión reducida de YouTube Lite  bajo el paradigma de bases de datos relacionales . Las reglas de negocio son las siguientes:

1. De cada usuario guardamos un código único, nombre, apellido, email (que es único), password, nombre de usuario (que es único), fecha de nacimiento, país, dirección, de la cual se almacena calle, número, ciudad, código postal, piso (que puede no existir) y departamento (que puede no existir).
2. Los usuarios pueden ser premium o free. Un usuario premium es el que tiene un abono mensual y no ve publicidades en los videos que reproduce. Para ello se almacenan los datos de la tarjeta de crédito con la que abona: nombre del titular (como figura en la tarjeta), DNI del titular, fecha de vencimiento, número de tarjeta
(que es único), banco y el código CVV de la misma. Las tarjetas pueden ser compartidas por varios usuarios pero un usuario tiene asignada una sola tarjeta.
3. De cada video se guarda un código numérico único, un título, una descripción (que puede no estar), una resolución, que puede tomar los siguientes valores: 1440p (2K): 2560 × 1440, 2160p (4K): 3840 × 2160, 720p (HD): 1280 × 720, 1080p (Full HD): 1920 × 1080, la ruta (url) de almacenamiento del archivo de video, duración del video, tres thumbnail, la cantidad de reproducciones, la cantidad de likes, la cantidad de dislikes.
4. Un video tiene un estado que puede tomar alguno de los siguientes valores: público, oculto y privado.
5. Un video puede tener muchas etiquetas escritas por el usuario que publica el video. Una etiqueta se identifica por un código numérico correlativo entre las etiquetas del usuario y un nombre de etiqueta. Tener en cuenta que el código de etiqueta como el nombre se pueden repetir en los distintos videos.
6. Un usuario puede crear un canal. Un canal tiene un código numérico único, un nombre, una descripción (que puede no estar) y una fecha de creación.
7. Para publicar videos el usuario debe crear obligatoriamente un canal previamente.
8. Interesa guardar quién es el usuario que publica el video y en qué fecha/hora lo hace.
9. Un usuario se puede suscribir a los canales de otros usuarios.
10. Un usuario puede darle un like o un dislike a cada video una única vez. Hay que llevar un registro de los usuarios que le han dado like y dislike a un determinado video y en qué fecha/hora lo hicieron. Estas acciones pueden revertirse.
11. Un usuario puede crear playlists con los videos que le interesan. Un mismo video puede pertenecer a distintas playlists del mismo usuario o distintos usuarios.
12. Cada playlist tiene un código numérico único, un nombre, una fecha de creación y un estado que indica que puede ser pública o privada.
13. YouTube te puede recomendar videos en función de los videos que has visto, por lo tanto, habrá que indicar qué videos están relacionados entre sí por sus contenidos similares.
14. Un usuario puede escribir comentarios en un video determinado. Cada comentario está identificado por un código único, el texto del comentario y la fecha/hora en la que se realizó. Estas acciones pueden revertirse. Un comentario puede tener comentarios (subcomentarios) de otros usuarios.
15. Un usuario puede marcar un comentario con un “Me gusta” o un “No me gusta”. Hay que llevar un registro de los usuarios que han marcado un comentario como Me gusta/No me gusta, y en qué fecha/hora lo hicieron. Estas acciones pueden revertirse.
16. Se deben almacenar los pagos mensuales de los usuarios premium, los mismos tienen una fecha de pago y un monto. Se sabe además que en una misma fecha realizan pagos muchos usuarios.
17. Los usuarios free, que no realizan abonos mensuales, ven publicidades en los videos que reproducen, y esto debe almacenarse. De las publicidades se sabe el nombre de la empresa, organización, etc. a la cual pertenece la publicidad, duración en segundos/minutos y la ruta de almacenamiento del archivo de video (no son videos de YouTube).
18. También deben almacenarse los videos que visualizan los usuarios premium, pero esta vez sin publicidades.
19. En las visualizaciones de videos de cualquier tipo de usuario debe almacenarse la fecha y la hora, teniendo en cuenta que un usuario puede ver el mismo video más de una vez y que un video puede ser visto por muchos usuarios.

## Caso Registro de las Personas de la Pcia. de Buenos Aires

El Registro Provincial de las Personas  tiene como responsabilidad primaria el registro en documentos de los hechos y actos que constituyan, alteren o modifiquen la identidad, el estado civil y la capacidad de las personas por medio de la elaboración de actas (de nacimiento, defunción, matrimonio o divorcio), Documentos Nacionales de Identidad (DNI), Pasaportes y Visas.

1. El DNI permite identificar a una persona física dentro del sistema y está compuesto por el número de DNI (único), número de trámite (único), CUIL (único), nombre y apellido, dirección, el sexo (M, F, X), la nacionalidad (ARGENTINO, EXTRANJERO),  si es o no donante de órganos (DONANTE, NO DONANTE), y la fecha de nacimiento. Tiene la fecha de emisión, la fecha de vencimiento, una foto (se almacena la url de la ubicación del archivo de la foto), firma y código de identificación digital (único).
2. La dirección del DNI tiene la calle, el número, piso y departamento, estos últimos pueden no corresponder. Además, se sabe la ciudad.
3. De las ciudades se almacena el código postal, que es único, nombre, que se puede repetir; y provincia.
4. El Pasaporte está asociado a un único DNI y posee los siguientes datos: número de pasaporte (único), fecha de expedición y expiración. Un DNI puede estar asociado o no a un pasaporte. Un pasaporte puede tener o no muchas visas.
5. De la visa se conoce su tipo, duración y un código (único). El tipo de visa puede ser de: (TRÁNSITO, TURISTA, TRABAJO o ESTUDIANTE). Pertenecen a un único pasaporte.
6. De los establecimientos (hospitales, registros civiles de cada ciudad, juzgados, etc.) se sabe el nombre y la dirección. El establecimiento está ubicado en una única ciudad.
7. En cuanto a las actas se conoce la ciudad en donde fue celebrada, el establecimiento en donde se llevó a cabo, la fecha y la hora. Poseen un número de acta que es único. Hay diferentes tipos de actas: de nacimiento, de defunción, de matrimonio y de divorcio.
8. Las actas de nacimiento están asociadas a un DNI, se conoce además a la madre, al padre y se debe almacenar la matrícula de la persona que asistió el parto (partera / partero).
9. Las actas de defunción están asociadas a un DNI, poseen la causa de defunción (NATURAL, NO NATURAL), la profesión (DESEMPLEADO, ESTUDIANTE, EMPLEADO) y el estado civil cuyo valor se obtiene de la siguiente forma:
    * SOLTERO: la persona fallecida no tiene acta de matrimonio.
    * CASADO: la persona fallecida tiene acta de matrimonio y no tiene acta de divorcio y el contrayente no tiene acta de defunción.
    * DIVORCIADO: la persona fallecida tiene acta de matrimonio con su respectiva acta de divorcio y no tiene otra acta de matrimonio vigente.
    * VIUDO: la persona fallecida tiene acta de matrimonio, no tiene acta de divorcio y su contrayente tiene acta de defunción anterior a la fecha de defunción de la persona fallecida.
10. De las actas de matrimonio se conoce a ambos contrayentes y a los dos testigos. El acta de matrimonio puede tener asociada o no un acta de divorcio.
11. De las actas de divorcio se conoce el periodo de unión, donde la fecha de inicio del periodo tiene que ser la fecha de acta del matrimonio y la fecha de fin debe ser posterior a la fecha de inicio y a los dos divorciantes. El acta de divorcio tiene asociada obligatoriamente el acta de matrimonio de los dos divorciantes.
12. Por otro lado, en los registros civiles hay empleados que se encargan de realizar las altas y modificaciones de las distintas actas. De cada empleado se conoce el DNI, legajo (único), el registro civil en donde trabaja, el cargo (ABOGADO, SECRETARIO, OFICINISTA, SUPERVISOR, ADMINISTRADOR) y uno a tres números de teléfono del cual se conoce su código de área, su número, y su detalle de contacto (PRINCIPAL, SECUNDARIO, EMERGENCIA).
13. Las modificaciones de las actas deben ser controladas por los empleados que son administradores antes de hacerlas efectivas en el sistema, para ello, se cuenta con un registro de la fecha, hora, minutos y segundos en las que las actas han sido modificadas por los empleados.
Estas modificaciones son controladas por un administrador que las avala antes de ser dadas de alta. Cada acta puede ser modificada más de una vez o no serlo.
14. Existen supervisores cuyo rol es supervisar a un grupo de empleados, y un empleado puede ser supervisado por un supervisor.

## Caso Distribuidora de Productos Alimenticios

Se desea realizar una base de datos destinada a una distribuidora de productos alimenticios  en la ciudad de Ushuaia. El objetivo de dicha base de datos es poder gestionar el funcionamiento general de la misma.
Las reglas de negocio son las siguientes:

1. La distribuidora cuenta con empleados. De todos ellos se almacena el apellido, el nombre, el DNI, CUIL, e-mail (que es único), dirección (calle, número, barrio), números de teléfono, fecha de inicio y fecha de fin (que puede no estar). También se debe almacenar el número de legajo, que es único.
2. Los empleados se dividen en cajeros, repositores, personal de maestranza, administrativos y choferes.
3. Hay empleados que son jefes de otros empleados.
4. Los administrativos son los encargados de generar los pedidos a los clientes que lo solicitan. A su vez también se encargan de realizar las compras de artículos a los proveedores.
5. Para realizar compras la distribuidora tiene contacto directo con proveedores de las marcas que ofrece en su local. De los proveedores se conoce el nombre, e-mail (que es único), dirección (localidad, calle, número, ciudad, código postal), razón social (que es única), números de teléfono y CUIT.
6. De los artículos se conoce su nombre, precio y código de barra que es único.
7. De las marcas se conoce el nombre que es único. Un artículo pertenece a una marca y una marca contiene muchos artículos.
8. Los empleados administrativos realizan compras a los proveedores. Una compra pertenece a un único proveedor, pero un proveedor puede participar o no de una compra, ya que en el sistema puede haber proveedores a los que aún no se les ha comprado ningún producto.
9. Cada compra la realiza un único empleado administrativo, pero éste realiza muchas compras.
10. De las compras a los proveedores se almacena su factura, la cual tiene un encabezado que consta del número de factura (único), fecha, monto total y los datos del proveedor (nombre, razón social, dirección, email, cuit, teléfonos). También contiene los renglones en donde se especifica el nombre del artículo, el número del renglón, marca, precio, cantidad y subtotal, que se calcula con la cantidad multiplicada por el precio. El monto total de la factura es la sumatoria de los subtotales de los renglones de la misma.
11. Se desea conocer la cantidad mensual comprada de cada artículo a cada proveedor.
12. De los clientes se guarda el nombre, un teléfono, e-mail (que es único) varias direcciones (localidad, calle, número, barrio, barrio), ya que, por ejemplo, un cliente puede tener domicilio fiscal de la empresa y el domicilio del depósito a donde van los pedidos que realiza, y, por último, el número de cliente que es único.
13. Existen dos tipos de clientes, algunos serán empresas de las cuales se almacena su CUIT y razón social y otras serán personas de las cuales se guarda el DNI y CUIL.
14. Los clientes solicitan pedidos, pero un pedido solo pertenece a un cliente.
15. Para cada pedido se tiene una cabecera que consta del número del pedido (único), el número de cliente, dirección de envío y fecha en que se solicitó el pedido, el cuerpo del pedido tiene varias líneas, en cada línea se detalla el nombre artículo pedido, el número de línea, precio, cantidad y subtotal que se calcula con la cantidad multiplicada por el precio. Se quiere almacenar el monto total del pedido, el cual se obtiene con la sumatoria de los subtotales de cada línea del pedido.
16. Cada pedido lo realiza un solo empleado administrativo.
17. La distribuidora cuenta con una flota de camiones para la distribución de los pedidos. De los camiones se conoce su matrícula (única), su capacidad y el tipo de carga que pueden transportar (alimentos no perecederos o productos refrigerados).
18. Por otra parte, los choferes son los que transportan los pedidos a ciertos clientes. Un pedido es transportado por un solo chofer.
19. Un chofer puede manejar varios camiones, mientras que un camión puede ser manejado por varios choferes. Cada camión se asigna a los choferes por un período de tiempo, esta información debe almacenarse.
20. De los choferes se almacenan los datos de su licencia de conducir, fecha de alta, fecha de vencimiento y categoría. Las categorías deben tomar los valores dados por la Agencia Nacional de Seguridad Vial, disponibles en:
[https://www.argentina.gob.ar/seguridadvial/licencianacional/clasesysubclases](https://www.argentina.gob.ar/seguridadvial/licencianacional/clasesysubclases)

## Caso Tu Cine

La empresa “Tu Cine” dispone de una red de cines en toda Argentina y desea informatizar su gestión. Para ello, es necesario diseñar una base de datos que cumpla con los siguientes requisitos:  

1. Debe almacenarse información de cada cine donde se incluya un código alfanumérico identificador, su nombre, dirección (calle, número, ciudad, código postal), teléfonos y correo electrónico (que es único).  
2. Cada cine dispone de un conjunto de salas de las cuales será necesario almacenar un código alfabético que se repite dentro de cada cine, el número de butacas que contiene y el tamaño en pulgadas de su pantalla de proyección.  
3. Cada butaca se identifica por el número de fila y el número de asiento que ocupa dentro de la sala.  
4. Cada cine dispone de unos pequeños bares de los que será necesario almacenar un código identificatorio y su nombre, que se puede repetir.  
5. Será necesario guardar la información de los productos que cada bar ofrece al cliente. De cada producto será necesario almacenar su código de barras único, nombre, precio, el tipo de producto del que se trata (comida o bebida) y la cantidad (stock) de que se tiene del mismo.  
6. Será necesario también, almacenar las películas que se presentan en la  cartelera. La información de cada película debe incluir un código alfanumérico identificatorio, su título, su director, actores que la protagonizan, breve descripción del argumento y el género cinematográfico al que pertenece. Además, se sabe si está disponible en las opciones 2D, 3D y/o 4D y si está doblada o no al español.
7. De cada género cinematográfico se tiene un código alfanumérico único y su descripción que puede tomar valores como thriller, western, comedia, drama, comedia romántica, terror, suspenso, etc.
8. Cada una de las películas incluidas en la cartelera se proyecta en determinadas proyecciones. Por tanto, será necesario almacenar la fecha, el horario y el precio de cada proyección (se considera que el precio es el mismo para todos los espectadores de una determinada proyección con independencia de la butaca que ocupen, la edad del espectador, sala, etc.). Una misma película se puede estar proyectando al mismo tiempo o no en diferentes salas del mismo o distinto cine.
9. Debe almacenarse información relativa a los empleados que trabajan en cada cine. Esta información incluye un legajo (que es único), DNI, nombre, apellido, fecha de inicio, fecha de fin, que puede no estar, teléfono móvil y opcionalmente correo electrónico.
10. Los empleados pueden trabajar en un bar o proyectar películas, pero no ambas cosas. Se quiere saber qué empleados trabajan en el bar y qué empleados se encargan de las proyecciones de las películas.
11. Cuando un cliente compra una entrada para ver una película el sistema registra esta entrada asignándole un código identificativo, la butaca que ocupará el cliente y el importe. En cada entrada sólo se reserva una butaca para ver una película en una determinada proyección. Sin embargo, un mismo cliente puede comprar varias entradas.  
12. El sistema debe almacenar de cada cliente un código identificativo, DNI, su nombre, apellido, teléfono móvil, correo electrónico y fecha de nacimiento.  
13. Los empleados también pueden ser clientes del cine.
14. Los clientes pueden comprar o no productos. A instancias de promociones que se enviarán por correo electrónico, se quiere mantener un historial de los productos comprados por los clientes, sabiendo que un cliente puede comprar un mismo producto más de una vez en distintas fechas (incluso un mismo día).
15. Hay ciertos empleados que supervisan a otros empleados.

## Caso Web de la NBA

Se busca crear una base de datos para una página web de la National Basketball Association (NBA) que brinda información de los partidos, estadísticas sobre los jugadores y los equipos; y, además, brinda noticias sobre el mundo de la NBA :

1. De los usuarios de la página se debe almacenar el nombre de usuario (que es único), una contraseña, un email (que es único), la nacionalidad, la fecha de nacimiento y una imagen de perfil (que puede no estar). Se almacena la url de la ubicación de la imagen.
2. Los usuarios pueden elegir a sus jugadores y a sus equipos favoritos para recibir las noticias que les interesan y también pueden contratar una suscripción, la cual le da acceso a contenido exclusivo.
3. De la suscripción se almacenan un número único, la fecha de inicio, la fecha de vencimiento y  está asociada a la tarjeta de crédito con la cual se abonan los pagos de la misma.
4. Las suscripciones además tienen pagos, de los que se guarda el monto, código de orden (que se repite dentro de las suscripciones), la fecha de pago y si está o no efectuado el pago.
5. La fecha de vencimiento de la suscripción se calcula sumando 30 días a la fecha de inicio de la misma. Además, se renueva mensualmente a no ser que el usuario la de de baja, en ese caso, debe almacenarse la fecha de la baja de la misma.
6. De la tarjeta de crédito se guarda el nombre del titular, que puede diferir del titular de la suscripción, el número de tarjeta (que es único), la entidad financiera (Visa, Cabal, Amex, Mastercard, etc.), la fecha de vencimiento y el código de seguridad, que es de tres dígitos. Además cada tarjeta debe quedar asociada al usuario para que pueda usarla en futuras compras. Una tarjeta puede ser compartida por más de un usuario de la página.
7. De los equipos hay que almacenar su nombre (que es único), ciudad, una imagen del logo, en qué conferencia está (Este o Oeste) y a qué división (Atlántico, Central, Medio Oeste, Noroeste, Pacífico, Sureste, Suroeste) pertenece.
8. Cada equipo está compuesto por el entrenador principal y de 12 a 17 jugadores.
9. De los jugadores se debe guardar el nombre, la fecha de nacimiento, fecha de fallecimiento (si es que falleció), la nacionalidad, la estatura, una imagen de perfil (se almacena la url de la ubicación de la imagen), el número de dorsal, la posición en la que juegan (PG, SG, PF, SF, C) y se debe saber para qué equipos jugó/juega.
10. Del entrenador se guarda su nombre, su nacionalidad , su fecha de nacimiento, fecha de fallecimiento (si es que falleció), una imagen de perfil (se almacena la url de la ubicación de la imagen) y a qué equipos dirigió/dirige.
11. Para que un jugador juegue en un equipo debe tener un contrato, de este último se sabe su período de vigencia, compuesto por una fecha de inicio y una fecha de fin, el tipo de contrato (Bird Rights, 1st Round Pick, Minimum Salary, MLE, Two-Way Contract, Sign and Trade, Mini MLE, Bird, Early Bird, Non Bird, Bi-Annual Exception, Room Exception) y el monto total. Se quiere saber la información de todos los contratos del jugador con los equipos en los que haya jugado y con el equipo que juega actualmente.
12. En un partido participan dos equipos (uno local y uno visitante) y 3 árbitros.
13. De los árbitros se debe guardar el nombre, la fecha de nacimiento, fecha de fallecimiento (si es que falleció), una imagen de perfil (se almacena la url de la ubicación de la imagen), la nacionalidad, los años de experiencia y el número de dorsal, el cual es único para cada árbitro activo, por lo que se debe guardar información para saber si está activo o no.
14. Del partido se guarda la fecha y hora en la que se juega, el resultado (puntos del visitante y puntos del local), que se calculan en función de la cantidad de puntos que realizó cada jugador; y las estadísticas de cada jugador que participa en ese partido (cuántos minutos jugó, cantidad de puntos, asistencias, faltas, rebotes, robos, tapones y pérdidas).
15. Un partido puede ser televisado por uno o varios medios de comunicación. De éstos últimos se debe saber si son de pago o libres, los países en los que se transmiten y el nombre que es único para cada medio.
16. Cada partido puede ser televisado más de una vez en el mismo medio o en distintos medios de comunicación. Deben almacenarse las distintas fechas y horas en que son televisados.
17. Los usuarios reciben noticias por email. De éstas se almacena un código único, un título, un texto, una fecha y un conjunto de imágenes (se almacena la url de la ubicación de cada imagen). Se debe saber qué noticias se enviaron a cada usuario, las cuales dependen de si tienen suscripción o no.
18. Hay noticias relacionadas con otras noticias, ya que relatan hechos de una misma historia.

## Caso Gimnasio Red Hot Arms

El 19/9/2022 fuimos contactados por nuestro cliente, Walter Patrón. Él se acercó con la idea de desarrollar un sistema para la modernización de los aspectos administrativos de su gimnasio llamado Red Hot Arms . Éste está situado en la localidad de Arrecifes sobre la calle Belgrano al 1500 y lleva 15 años brindando servicios a la comunidad.
El gimnasio comenzó como una simple galería con equipamiento y maquinaria básica que con el tiempo se fue mejorando y ampliando para poder proveer más prestaciones. Al día de hoy cuenta con más de 50 máquinas y un promedio de 300 clientes.
Desde sus orígenes, el gimnasio ha llevado registro de toda la información administrativa de forma manual en planillas de Excel, guardando registros como información de las y los clientes, información del equipo de entrenamiento, información de las clases que se ofrecen en el mismo, información acerca de las máquinas y el estado de éstas. El propósito actual del cliente es hacer el paso a un sistema que facilite y mejore el almacenamiento, el procesamiento y consulta de esta información.
Para ello, nos ha brindado las características requeridas para la construcción del mismo. Comenzaremos con el diseño de la base de datos, las reglas de negocio son las siguientes:

1. De cada cliente que va al gimnasio se necesita conocer el tipo de plan,  tipo de seguimiento (personalizado, general), como también el DNI, nombre, apellido, fecha de inicio, fecha de baja, si es que no es más cliente, fecha de nacimiento, dirección, número de celular y correo electrónico (que es único).
2. De la dirección se almacena la calle, número, piso y depto. Estos dos últimos datos pueden no corresponder.
3. El tipo de plan de cada cliente le da accesos diferentes según su nivel. El plan básico le da acceso sólo al gimnasio y a sus máquinas. El plan bronce también da acceso al gimnasio, sus máquinas y a una clase a elección. Y el plan oro le da acceso al gimnasio, sus máquinas y a todas las clases que quiera. En cualquiera de estos tres planes el seguimiento puede ser libre o tener seguimiento personalizado por una persona del equipo del gimnasio.
4. De cada entrenador/a que trabaja en el gimnasio se debe conocer la modalidad, títulos que posee, los horarios y días en lo que trabaja, como también su DNI, nombre, apellido, fecha de inicio, fecha de baja, si es que no trabaja más en el gimnasio, fecha de nacimiento, dirección, número de celular  y correo electrónico  (que es único). Su modalidad determina si es un entrenador/a general, que atiende a la totalidad de clientes por igual, o personal que hace seguimiento detallado a una sola persona (o grupo pequeño) a la vez.
5. De cada recepcionista se debe conocer horarios y días de trabajo, como también, su DNI, nombre, apellido, fecha de inicio, fecha de baja, si es que no trabaja más en el gimnasio, fecha de nacimiento, dirección, número de celular y correo electrónico  (que es único).
6. De los días y horarios que trabaja una persona en el gimnasio se almacenan los días (lunes, martes, miércoles, jueves, viernes, sábado) que trabaja en el gimnasio y el horario, por ejemplo, lunes de 08:00 a 16:00, martes de 14:00 a 22:00, etc.
7. Los empleados del gimnasio pueden ser clientes.
8. El gimnasio está dividido en áreas, de estas se debe saber su nombre y capacidad (cantidad de personas que puede contener). El nombre del área no puede repetirse. Estas áreas pueden tener tanto máquinas, como equipos anaeróbicos o equipos de peso.
9. De cada máquina se registra el nombre, código único, marca y área en donde se encuentra.
10. En el gimnasio hay diferentes tipos de equipamiento anaeróbico. Hay sogas de saltar, elásticos, bolsas de boxeo, peras, pelotas de esferodinamia y pelotas medicinales. De cada uno se debe almacenar un código único para identificarlos, su tipo, su peso y área en donde se encuentra.
11. En el gimnasio, también hay diferentes tipos de equipamiento de peso. Hay mancuernas, discos, barras, bolsas de peso corporal y pesas rusas. De cada uno se debe almacenar un código único para identificarlos, su tipo, su peso y área en donde se encuentra.
12. Se dictan distintos tipos de clases, los cuales son: yoga, crossfit, spinning, zumba, funcional y kick boxing con sus respectivos días y horarios. Por ejemplo, una clase de yoga es los lunes de 16:00 a 17:00 y otra clase de yoga es los miércoles de 18:00 a 19:00. Las/os entrenadoras/es imparten las clases y cualquier cliente puede recibirlas. Cada clase es impartida por un solo entrenador.
13. En el mostrador del gimnasio hay una parte reservada para la venta de diversos productos saludables. Cada producto tiene un tipo (bebidas o snacks), un código de barras único, precio y nombre.
14. Se solicita llevar un registro de cuándo se realizó cada venta, es decir, se debe saber la persona a la cual se le realizó la venta, la fecha, los productos comprados, cantidad de cada producto y el monto total de la venta.  El monto total se calcula sumando los productos matemáticos del precio de cada producto por la cantidad comprada. Una venta se identifica por un código numérico único.
15. Las y los clientes pagan mensualmente una cuota. A cada pago se le debe asignar un número de pago, que se repite para cada cliente, su monto, fecha de vencimiento y fecha efectiva del pago, que no se carga en el sistema hasta que el cliente paga la cuota efectivamente.
16. Es tarea de las/os recepcionistas limpiar las áreas del gimnasio. Se sabe qué recepcionista limpia cada área. En cada turno las áreas son limpiadas por distintos recepcionistas.
17. Es tarea de las/os entrenadoras/es mantener las máquinas. Para ello se debe almacenar la fecha en que cada entrenador le hace la revisión técnica a cada máquina y una breve descripción de la tarea realizada y los posibles problemas encontrados, sabiendo que, una misma máquina puede ser revisada por la misma persona en distintas fechas.
18. Las/os entrenadoras/es pueden ser jefes de otros entrenadores.
19. De los clientes que solicitan un seguimiento personalizado, se deben almacenar las máquinas que utilizan y los entrenadores que hacen seguimiento. Para lo cual se almacena la fecha y hora de los seguimientos realizados por los entrenadores a los clientes en determinadas máquinas.

## Caso Twitter

Twitter  es una de las más grandes redes sociales. En ella, la principal función es que cualquiera puede subir “tweets” con texto, fotos, videos u otras funciones; y a la vez interactuar con otras personas a través de sus “tweets”. Esta red social se basa más en una comunicación escrita, a diferencia de otras redes en las que predominan otro tipo de publicaciones, como Instagram que se basa en fotos.
Para crear una base de datos para Twitter con el paradigma  de bases de datos relacionales, contaremos con los siguientes requisitos para nuestro sistema:

1. Twitter tiene usuarios. Estos deben ser alguno de estos tres tipos obligatoriamente: usuario free, usuario verificado y usuario premium. Además, si un usuario es de cierto tipo no puede ser de otro.
2. Cada usuario (los 3 tipos) cuenta con las siguientes características: nombre de usuario, arroba de usuario, el cual es único, un código, también es único, teléfonos, correo electrónico, que es único, fecha de creación, fecha de nacimiento, ubicación que está compuesto por el país, la provincia y la ciudad, idiomas, género, que puede ser: M, F o X y la edad, la cual debe de ser mayor o igual a 13 años debido a que no se pueden permitir niños en una red social. Además, la edad se actualiza cada día respecto al país de ubicación de la persona.
3. Un usuario (los 3 tipos) pueden seguir y ser seguidos por otros usuarios.
4. A los usuarios free les aparecen publicidades durante su “scroll”, es decir, cuando baja a través de la app. Estas publicidades son tweets y tiene un precio por visualización asociado el cual se decide en un acuerdo previo. Además, tiene cierta frecuencia, lo cual indica cuán frecuente lo visualizarán los usuarios y un código único para identificarlo.
5. Los usuarios verificados son aquellos que son personas muy conocidas, como famosos u organizaciones conocidas, y se verifica que esa cuenta es la de la persona u organización quien dice ser. Tienen una fecha de verificación, la cual se usa para mostrarla en el perfil y dar a conocer desde hace cuánto está verificada esa cuenta.
6. Los usuarios premium realizan una suscripción que se renueva mensualmente, la cual se identifica con un código único. Además, se conocen otros datos: fecha de inicio de la suscripción, fecha de renovación del servicio y una forma de pago, que puede ser mediante tarjeta de crédito o PayPal. La fecha de renovación del servicio se calcula de forma automática sumando treinta días a la fecha de suscripción.
7. Las suscripciones registran pagos mensuales. Nos interesa llevar un registro de todos los pagos que un usuario premium ha ido realizando durante el período de tiempo que está suscripto. De cada pago se guarda la fecha de vencimiento, un número de orden correlativo dentro de cada suscripción, un monto y la fecha efectiva de pago, que si aún no ha sido abonado el pago, ésta no contendrá ningún valor.
8. De las tarjetas de crédito se conoce: el número de tarjeta, el cual es único, el banco que la otorgó, mes y año de vencimiento y el código de seguridad, nombre del titular (como figura en la tarjeta) y entidad financiera de la misma, las cuales pueden ser: VISA, Cabal, Mastercard, American Express, Nativa, Naranja, etc. Se acepta solo una tarjeta por usuario, pero la tarjeta puede ser usada por muchos usuarios. Del Paypal se conoce el nombre de usuario, el cual es único. Se acepta solo un Paypal por usuario, pero el Paypal puede ser usado por muchos usuarios.
9. Además, un usuario puede tener solo una tarjeta o solo un Paypal asociado, nunca ambos.
10. Los usuarios publican Tweets. Los tweets tienen un código asociado al código del autor, el texto, la fecha de publicación, la cantidad de likes, de retweets, de comentarios, de reproducciones y de elementos guardados, una ubicación con país y provincia (que puede ser diferente al del autor, por si la persona por ejemplo tuitea durante un viaje) y un autor (usuario asociado). Pueden contener contenido multimedia asociado, hasta 4 fotos o vídeos. Además, los tweets tienen al menos un tema, que es respecto a que trata el tweet y con esto podemos asociar otros tweets. Un usuario puede tener varios tweets y un tweet pertenece a un único usuario.
11. Los usuarios pueden “likear”, “guardar” y “retuitear” tweets, pero solo una vez por cada tweet. Además, pueden sacar este “like”, “guardado” y “retweet”.
12. Los usuarios pueden responder Tweets. Cuando respondes un Tweet se crea otro Tweet.
13. Los usuarios pueden seguir “temas” que son tweets de cierto tipo. Además, si interactúan con tweets de ciertos temas, se les recomienda otros tweets del mismo tema. Los temas se relacionan entre sí. Cada tema tiene un nombre único, que es de lo que se trata el tema.
14. Los usuarios forman parte de chats. Los chats se crean cuando una persona envía un mensaje a otra persona, así que los chats tienen una fecha de creación. Además, el chat se identifica con un código.
15. Los distintos usuarios pueden enviar distintos mensajes a distintos chats. Los chats están conformados por 2 o más usuarios. También se pueden enviar tweets por chat.
16. De los mensajes se guarda el texto, el cual puede no estar si se envía un tweet como mensaje, la fecha y un código que se asocia al código del usuario que haya enviado el mensaje. Además, los mensajes son vistos o no.
17. Los usuarios pueden mencionar a otros usuarios en sus tweets.
18. Los tweets pueden incluir hashtags que permiten a los usuarios buscar tweets específicos. Cada hashtag tiene un índice de popularidad que indica cuántos tweets lo utilizan, un texto asociado que es respecto a sobre qué es el hashtag y un código único.
19. Cuando se buscan tweets por medio de un hashtag, se guarda la fecha de esa búsqueda, y un usuario puede buscar varias veces tweets por medio de un mismo hashtag en distintas fechas.

## Caso Bar Ghins

El bar-pub juninense “Ghins”  desea crear un nuevo sistema de administración y somos los convocados para llevar a cabo la base de datos que utilizará este nuevo sistema ya que el que utilizaban anteriormente ya no les convence. Para lo cual se tienen los siguientes supuestos semánticos:

1. El bar cuenta con varios empleados: mozos, encargados, cocineros y personal de limpieza. De todos ellos se conoce el nombre, legajo, que es único,  sueldo y en qué turnos trabajan.
2. De cada turno se conoce día, hora de entrada y de salida.
3. Ningún empleado trabaja los lunes.
4. Hay encargados de mozos y encargados de cocineros. Para todos ellos se lleva registro del período de tiempo en el que están en el cargo, el cual tiene una fecha de inicio y una fecha de fin, esta última puede no conocerse si se trata del período vigente.
5. El bar vende dos tipos de productos: bebidas y platos, de estos se conoce una descripción, un nombre, que es único y tienen un precio. Además de esto las bebidas cuentan con un código de barra único. De los platos se sabe si es entrada, minuta, plato principal o postre.
6. Los platos pueden componer a otros platos que funcionan como combos.
7. Los platos son preparados por los cocineros con ciertas materias primas, de estas últimas se conoce un código único, un nombre, un precio y también los proveedores encargados de venderlas al local.
8. El proveedor cuenta con uno o más teléfonos, email que es único, nombre y CUIT. Distribuyen tanto materias primas como bebidas.
9. Los mozos son los que se encargan de atender y llevar los productos a las mesas.
10. Las mesas cuentan con un número que las identifica y una determinada capacidad de personas que se pueden ubicar en ellas (2, 4 o 6).
11. Cada cliente registrado en el sistema cuenta con un nombre, una dirección (calle, número, y opcionalmente departamento y piso) y uno o más teléfonos.
12. Cuando un cliente paga el servicio (reserva efectiva o delivery) se genera una factura. De éstas se conoce el cliente, el monto total, la fecha, el método de pago, que puede ser efectivo, crédito, débito o transferencia y posee un número que es único.
13. La factura está conformada por líneas. Cada línea detalla a uno de los productos de la venta, indicando el precio de venta, la cantidad vendida y el subtotal de cada línea. Además, las líneas poseen un número de línea que se repite para cada venta.
14. El subtotal de la línea se calcula multiplicando el precio del producto por la cantidad.
15. El monto total de la venta se calcula sumando los subtotales de las líneas de la venta.
16. El bar también realiza pedidos por deliverys, los cuales están tercerizados. Se conoce a qué cliente es enviado, qué productos son enviados, a qué hora se realizó, un comentario opcional acerca del mismo (por ejemplo, una aclaración acerca de la vivienda del cliente) y un código identificatorio.
17. Cada pedido por delivery también genera una factura.
18. Un cliente puede pedir una reserva para una mesa para un día y una hora en particular. La reserva tiene un número único que la identifica, una fecha de alta, la mesa y la fecha de la reserva (día y hora en que se reserva la mesa).
19. Cada reserva pertenece a un único cliente y puede ser efectiva (que se tomó la mesa que se reservó,  se dio el servicio y se facturó), vigente (que aún está pendiente de ser efectiva)  o cancelada. Las reservas que son efectivas son las únicas facturadas.

## Caso Negocios de Venta de Ropa

Hemos sido convocados por una cadena de Negocios de Venta de Ropa  para cambiar los sistemas de software existentes. Se nos ha designado dentro del equipo para realizar el diseño de la base de datos, para ello contamos con los siguientes supuestos semánticos:

1. El negocio tiene múltiples sucursales distribuidas por todo el país. En las sucursales trabajan distintos empleados. Los empleados pueden ser vendedores o encargados de la sucursal. Cada empleado trabaja en una sola sucursal.
2. Cada sucursal tiene muchos vendedores pero un solo encargado.
3. De una sucursal se sabe la ciudad, código postal, dirección, email y los números de teléfono.
4. De los empleados interesa saber el nombre, apellido, DNI, CUIL, legajo (que es único), la dirección que está compuesta por calle, número, depto y piso, estos dos últimos datos pueden no estar, ciudad, código postal, número de teléfono, email (que es único), fecha de alta y la fecha de baja en caso de que ya no forme parte de la planta de empleados.
5. De los clientes se quiere saber el nombre, un código único de cliente, DNI, fecha de nacimiento, dirección, fecha de alta, email (que es único) y un número de teléfono, que puede ser compartido con otro cliente.
6. Los vendedores realizan ventas de ropa a clientes y éstas se facturan. Las facturas se identifican por un número de factura que es único, tienen un código de barra que también es único, el monto total y el cliente al cual se le realiza la venta.
7. Las facturas se componen de renglones. Cada renglón tiene un número correlativo dentro de cada factura, el producto comprado, el precio y la cantidad del mismo. El subtotal del renglón se calcula multiplicando el precio del producto por la cantidad.
8. El total de la factura se calcula sumando los subtotales de los renglones de la misma.
9. De la factura también interesa almacenar las formas de pago con la cual se realizó, que puede ser al contado o con tarjeta. Una factura puede abonarse con más de una forma de pago.
10. Una factura contiene distintos pagos, dependiendo de las formas de pago que se utilicen para abonarla.
11. De un pago se almacena el número de pago, que es único dentro de  la factura, posee la fecha en que se realizó y el monto, ya que una factura puede tener más de un pago.
12. Los pagos al contado pueden tener descuento o no (que se resta al monto del pago).
13. Los pagos con tarjeta se realizan con una sola tarjeta, tienen un recargo (que se suma al monto del pago) y la cantidad de cuotas (1,3 o 6).
14. Las tarjetas poseen nombre del titular, número que es único, CVV, banco al que pertenecen, financiera (Visa, Mastercard, American Express, Cabal, Naranja o Nativa) mes y año de vencimiento.
15. Una tarjeta está asociada a un único cliente, pero cada cliente puede tener asociadas muchas tarjetas.
16. Los encargados compran los productos. Interesa saber la fecha que se realiza cada compra y la cantidad del producto, sabiendo que un producto es comprado por los encargados en distintas fechas.
17. De los proveedores conocemos su nombre, CUIT, dirección, email (que es único) y número de teléfono.
18. De los productos se almacena nombre, talle, su precio de costo y de venta, la marca y un código único. Los mismos se dividen en categorías. De las categorías nos interesa guardar su nombre, el cual será único y una descripción.
19. Una categoría puede ser subcategoría de otra.
20. Cada producto es vendido por un único proveedor, pero los proveedores pueden vender muchos productos.
21. Se debe almacenar el stock (cantidad) de los productos que tiene cada sucursal, sabiendo que un mismo producto puede venderse en distintas sucursales.
22. Una sucursal puede tener promociones de distintas categorías de ropa. Por ejemplo, remeras o camperas se ponen en promoción por fin de temporada. De las promociones se desea almacenar un código de promoción único, el descuento, una descripción, las formas de pago (al contado o con tarjeta) y las categorías que promociona. También se desea almacenar la fecha de inicio y de fin de las promociones.

## Caso Spotify

Imaginemos cómo sería un modelo sencillo de la base de datos para Spotify  con el paradigma de bases de datos relacionales. Para ello, tendremos los siguientes requerimientos para el sistema :

1. Existen dos tipos de usuarios: usuario free y usuario premium.
2. De cada usuario guardamos un código único, email (que no se repite), password, nombre de usuario, fecha de nacimiento, fecha de alta, sexo, que puede tomar los valores: M, F o X, fecha de baja, si es que el usuario se dio de baja del servicio, país, dirección, ciudad y código postal.
3. La dirección está compuesta por calle, número, barrio, depto y piso. No todas las direcciones tendrán barrio, depto y piso.
4. Los usuarios premium realizan suscripciones. Los datos necesarios que habrá que guardar para cada suscripción son: fecha de inicio de la suscripción, fecha de renovación del servicio y una forma de pago, que puede ser mediante tarjeta de crédito o PayPal.
5. La fecha de renovación del servicio se calcula de forma automática sumando treinta días a la fecha de suscripción.
6. De las tarjetas de crédito de los usuarios premium se debe almacenar el número de tarjeta (que es único), el banco que la otorgó, mes y año de vencimiento y el código de seguridad, nombre del titular (como figura en la tarjeta) y entidad financiera de la misma, las cuales pueden ser: VISA, Mastercard o American Express. Se acepta solo una tarjeta por usuario, pero la tarjeta puede ser usada por muchos usuarios.
7. De los usuarios que pagan con PayPal se almacena el nombre de usuario de PayPal.
8. Nos interesa llevar un registro de todos los pagos que un usuario premium ha ido realizando durante el período de tiempo que está suscripto. De cada pago se guarda la fecha, un número de orden, que se repite dentro de los pagos de cada usuario, y un monto.
9. Un usuario puede crear muchas playlists. De cada playlist guardamos un título, la cantidad de canciones que contiene, un código identificador único y una fecha de creación.
10. Un usuario puede utilizar distintas playlists de otros usuarios.  
11. Un usuario premium puede seguir y ser seguido por otros usuarios.
12. Cuando un usuario borra una playlist, ésta no se borra del sistema, sino que se marca como que ha sido eliminada. De este modo el usuario puede volver a recuperar sus playlists en caso de que las haya eliminado por error. Es necesario almacenar la fecha en la que una playlist ha sido marcada como eliminada.
13. Podemos decir que existen dos tipos de playlists: activas y borradas.
14. Una playlist que está activa puede ser compartida con otros usuarios, esto quiere decir que otros usuarios pueden añadir canciones en ella. En una lista compartida nos interesa saber qué usuario ha sido el que ha añadido cada canción y en qué fecha lo hizo. Sabiendo que si una canción es añadida por un usuario ya no puede ser añadida por otro.
15. Una canción sólo puede pertenecer a varios álbumes. Un álbum puede contener muchas canciones. Un álbum ha sido publicado por uno o varios artistas. Un artista puede haber publicado muchos álbumes.
16. De cada canción guardamos un código único, un título, que se puede repetir, la letra, una duración y el número de veces que ha sido reproducida por los usuarios de Spotify.
17. De cada álbum guardamos un código único, título, que es único, año de publicación y una imagen con la portada.
18. De cada artista guardamos un código único, nombre,  género y una imagen del artista.
19. Se debe almacenar información de los géneros musicales. Éstos pueden ser clásica, pop, jazz, electrónica, indie, reggeaton, rock, flamenco, etc.
20. Cada canción es interpretada por uno o varios artistas.
21. Un usuario puede seguir a muchos artistas.
22. Un artista puede estar relacionado con otros artistas que hagan música parecida. De modo que, Spotify pueda mostrarnos un listado de artistas relacionados con los artistas que nos gustan.
23. También nos interesa guardar cuáles son los álbumes y las canciones favoritas de un usuario. Un usuario puede seleccionar muchos álbumes y muchas canciones como favoritas.
