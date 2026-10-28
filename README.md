Hola este es mi segundo analisis iniciando el día 26 de octubre, yo espero no acabarlo hoy.

Tenemos una data de 180 mil datos aproximadamente con 53 columnas de las cuales podemos observar que la data es de pedidos por cliente.

Iniciaremos resaltando las columnas que nos pueden dar alto valor.

El tipo de pago, cual es el tipo que mas se ocupa?  **Type**
los dias real de envio vs los dias programados **Days for shipping (real)** **Days for shipment (scheduled)**
El status **Delivery Status**
que es el delivery risk? **Late_delivery_risk**
por categoria **Category Name**
por ciudad y pais cuantos clientes tenemos? **Customer City** **Customer Country**
la ciudad de donde salio la orden 
**Order Country**
order date **order date (DateOrders)**
order id **Order Id**
que es sales per customer **Sales per customer**
order quantity y order product price y sales **Order Item Product Price**
**Order Item Quantity**
como se calcula el order item total **Order Item Total**
el orer status **Order Status**
shiping date**shipping date (DateOrders)**
modo de shipping **Shipping Mode**

ya teniendo las columnas son las que pienso principalmente para empesar un EDA

Iniciemos por donde estamos.
Creamos un nuevo dataset solo con las columnas que pensamos que seran mas utiles.

Analicemos las ordenes por pais, que pais tiene mas ordenes.
las columnas que vamos a necesitar son:
1. Order Country
2. Order id
3. Order Status

asi calculamos solo las que ya estan entregadas pero sin dejar de lado de ver el sesgo de cuantas ordenes entregadas y cuales no.

Observando el resultado podemos ver que el pais con mas ordenes es Estados unidos. Sin embargo seguramente es una respuesta que ya tiene los stakeholders, pero podemos sacar una tabla de cuales son los paises que tienen mas ordenes con status diferentes a COMPLETE.

No entraremos tanto en detalle con los status ya que necesitamos mas conocimiento de cada uno de los status sin embargo podemos calcular todas los status raros por pais.

En los Status quitando el **COMPLETE** podemos observar que el que predomina es **PENDING PAYMENT** con un 33.66% con 14382 ordenes.

Sin embargo primero revisemos si todas estas categorias tienen un Delivery Status que nos diga que fueron entregados al cliente.
Late delivery
Advance shipping
Shipping on time
Shipping canceled

Estos son los status que tenemos con el Delivery Status, observando los delivery Status de Pending Payment nos dice que la mayoria se enviaron tarde pero aun no nos han pagado.

Esto quiere decir que muchas ordenes quedan pendiente de pago pero la pregunta real es entregamos esas ordenes?



**Lecciones aprendidas**

En esta lección aprendimos a que no solo se trata de agarrar la data y programar sino en base a los kPIs aprender y analizar los resultados y de ahi encontrar la pregunta base.
Se programar y se usar pandas son embargo no tiene un hilo sigo analizando nada mas y no reviso los numeros, en base a los KPIs puedo encontrar la pregunta base de analisis y de ahi buscar areas de oportunidad.

Debo preguntarme que le importa al negocio, normalmente le importa, el servivio, calidad, ventas, etc.
Define metas de los objetivos o KPIs si es que aun no existen eso te ayuda para encontrar areas de oportunidad.

**Conclusion**
En conclusion el apartado de programación ya lo tienes bien enfocado, pero al crear un analisis de impacto estamuy verde no solo se trata de rogramar sino tambien se trata de lo que vas a entregar en base a los KPIs.
Debes tener un plan, una metodologia para generar un analisis de impacto, no solo se trata de programar o contestar preguntas.
Debes tener un enfoque hacia donde vas y que haras para generar impacto.

Recuerda
1. Define que vas analizar antes de saltar a la data
2. Lo que analizaras como se ve en los kPIs, si no tienes define KPIs con metas y en base de eso analiza
3. Recuerda las preguntas bases: **Que paso?**, **Por que paso?**, **Que va a pasar?** y **Que hacemos?**
    Pero para llegar a eso debemos tener primero que medir y eso nos ayuda los KPIs para tener un inicio y una pregunta base no solo analizar por analizar

En conclusión definimos que sabemos programar por lo menos lo basico y como hacerlo pero la metodologia es lo que debemos reforzar.
