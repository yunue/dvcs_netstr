# dvcs_netstr

Comprobación del análisis de red a (Git/Mercural)

Este apartado, contiene las instrucciones para replicar los resultados del análisis de red utilizados en este trabajo. Las herramientas de comprobación fueron Neo4j (https://neo4j.com) para replicar la estructura global del grafo de colaboración, y # # # Cytoscape (https://cytoscape.org) para verificar los patrones de conexión. 
## a) Comprobación del ordenamiento topológico
En primer lugar, es recomendable considerar que cada uno de los patrones que se analizan representan acciones de los usuarios que en conjunto definen la estructura de un grafo de colaboración.  En ese sentido, la comprobación topológica se basa en identificar el orden de los enlaces y definir la relación que conecta las acciones de los usuarios.
Para este propósito, se siguieron los siguientes pasos: 1) crear proyecto en Git / Mercurial, 2) importar los registros de actividad del proyecto a una base de datos orientada a grafos (en este caso Neo4j) y 3) utilizar el orden de los registros como referencia para definir la relación “padre-hijo” en la base de grafos. Una vez replicada la estructura global de la red, se puede identificar el orden de los vértices, y verificar que la relación de los enlaces coincida con el orden de los registros del grafo de colaboración. 

  Durante el procedimiento metodológico se argumentó que la colaboración distribuida depende de la forma en la que se organiza el trabajo de los colaboradores, ya que a través del análisis de esos patrones se identifica el funcionamiento de los componentes que sustentan este tipo de colaboración descentralizada. La Figura 6 ilustra el antes y el después de establecer tales relaciones entre los registros de trabajo, que una vez establecidas, dan forma a la estructura de la colaboración distribuida.
Gráfico 6. La captura de pantalla ilustra el antes (a) y después (b) de establecer la relación padre-hijo para los elementos del grafo de colaboración

## b) Comprobación de los patrones de sincronización
Una vez completado el paso anterior, es posible comprobar los patrones de sincronización. En este caso, se procede exportando el grafo de colaboración a una herramienta de análisis de red social. En particular, Cytoscape permite importar el proyecto directamente de Neo4j a través de la aplicación “cyNeo4j”. Una vez importado, se despliegan los paramentos relacionados con la conexión de los elementos en la red por medio de la herramienta SNA. Finalmente, los patrones de conexión para cada una de las acciones se pueden clasificar con base al grado de sus predecesores inmediatos (indegree) y el de los sucesores inmediatos (outdegree) ya que el flujo de un proyecto de colaboración distribuida se puede observar a través de los patrones de conexión que los conforman. 

## Los patrones que conectan el flujo de colaboración de un proyecto distribuido. 

Para este ejemplo, la estructura se constituye de tres diferentes flujos (versiones) señalados por las letras “a”, “b”, y “c”. En donde el flujo “a” representa el proyecto maestro, puesto que no tiene predecesores y de ahí se desprende “c”; mientras que el flujo “b” representa la unión de los diferentes flujos de trabajo “a” y “b”. También se puede observar que el trabajo de todas las líneas se encuentra indirectamente integrado sobre el flujo de trabajo maestro “a”.
Gráfico 7. La captura de pantalla detalla el grafo de colaboración, y los atributos de conexión para los registros de trabajo

  A través de este modelo, se puede sustentar la participación simultánea de múltiples colaboradores sobre un mismo proyecto, y al mismo tiempo, sin que ocurran problemas de concurrencia. A pesar de que el paradigma de colaboración distribuido aún es considerado un tema novedoso vinculado al formato digital, también es cierto que este tiene potencial para marcar una pauta y poner en perspectiva diversos dilemas que envuelve un tema tan importante para nuestra sociedad como lo es la colaboración.1

