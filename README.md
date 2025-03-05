1. Importar la biblioteca

Antes de crear gráficos, necesitas importar matplotlib.pyplot:

python
Run
Copy code
1import matplotlib.pyplot as plt
2. Crear gráficos básicos

Gráfico de líneas

python
Run
Copy code
1# Datos
2x = [1, 2, 3, 4, 5]
3y = [2, 3, 5, 7, 11]
4
5# Crear gráfico de líneas
6plt.plot(x, y)
7plt.title('Gráfico de Líneas')
8plt.xlabel('Eje X')
9plt.ylabel('Eje Y')
10plt.show()
Gráfico de dispersión (scatter)

python
Run
Copy code
1# Datos
2x = [1, 2, 3, 4, 5]
3y = [2, 3, 5, 7, 11]
4
5# Crear gráfico de dispersión
6plt.scatter(x, y)
7plt.title('Gráfico de Dispersión')
8plt.xlabel('Eje X')
9plt.ylabel('Eje Y')
10plt.show()
Gráfico de barras

python
Run
Copy code
1# Datos
2categorías = ['A', 'B', 'C', 'D']
3valores = [3, 7, 5, 2]
4
5# Crear gráfico de barras
6plt.bar(categorías, valores)
7plt.title('Gráfico de Barras')
8plt.xlabel('Categorías')
9plt.ylabel('Valores')
10plt.show()
Gráfico de barras horizontales

python
Run
Copy code
1# Crear gráfico de barras horizontales
2plt.barh(categorías, valores)
3plt.title('Gráfico de Barras Horizontales')
4plt.xlabel('Valores')
5plt.ylabel('Categorías')
6plt.show()
Histograma

python
Run
Copy code
1# Datos
2data = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 5]
3
4# Crear histograma
5plt.hist(data, bins=5)
6plt.title('Histograma')
7plt.xlabel('Valores')
8plt.ylabel('Frecuencia')
9plt.show()
Gráfico de pastel (pie chart)

python
Run
Copy code
1# Datos
2sizes = [15, 30, 45, 10]
3labels = ['A', 'B', 'C', 'D']
4
5# Crear gráfico de pastel
6plt.pie(sizes, labels=labels, autopct='%1.1f%%')
7plt.title('Gráfico de Pastel')
8plt.show()
3. Personalización de gráficos

Cambiar el color y el estilo de línea

python
Run
Copy code
1plt.plot(x, y, color='red', linestyle='--', marker='o')
2plt.title('Gráfico Personalizado')
3plt.show()
Agregar una leyenda

python
Run
Copy code
1plt.plot(x, y, label='Datos 1')
2plt.plot(x, [i**2 for i in x], label='Datos 2')
3plt.title('Gráfico con Leyenda')
4plt.xlabel('Eje X')
5plt.ylabel('Eje Y')
6plt.legend()
7plt.show()
Guardar un gráfico

python
Run
Copy code
1plt.plot(x, y)
2plt.title('Gráfico Guardado')
3plt.savefig('grafico.png')  # Guarda el gráfico como archivo PNG
4plt.show()
4. Subgráficos

python
Run
Copy code
1# Crear subgráficos
2fig, axs = plt.subplots(2, 2)  # 2 filas, 2 columnas
3axs[0, 0].plot(x, y)
4axs[0, 0].set_title('Gráfico 1')
5axs[0, 1].bar(categorías, valores)
6axs[0, 1].set_title('Gráfico 2')
7axs[1, 0].scatter(x, y)
8axs[1, 0].set_title('Gráfico 3')
9axs[1, 1].hist(data)
10axs[1, 1].set_title('Gráfico 4')
11plt.tight_layout()  # Ajusta el espaciado
12plt.show()
5. Estilos de gráficos

Puedes cambiar el estilo de los gráficos utilizando plt.style.use():

python
Run
Copy code
1plt.style.use('ggplot')  # Cambia el estilo a 'ggplot'
2plt.plot(x, y)
3plt.title('Gráfico con Estilo ggplot')
4plt.show()
