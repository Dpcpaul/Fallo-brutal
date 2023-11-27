# Esta es la gráfica del PIA 
El código es: import matplotlib.pyplot as plt

productos = ['Luces Navideñas', 'Papá Noel Inflable', 'Guirnalda Navideña', 'Guirnalda de Luces', 'Decoración de Porche', 'Juego de Fundas de Almohada', 'Cajas de Navidad (Adorno)', 'Cascabeles Navideños', 'Muñecos de Peluche', 'Colgantes Navideños', 'Nieve Artificial', 'Lámpara de Seda', 'Manteles Ind. 6 Pzas.', 'Kit 6 Cascanueces', 'Estrella Para árbol de Navidad']
precios = [230, 1540, 430, 160, 230, 180, 440, 100, 300, 215, 350, 110, 200, 220, 230]

fig, ax = plt.subplots()

bars = ax.bar(productos, precios, color=['red', 'blue', 'purple', 'orange', 'green'])

ax.set_ylabel('Precio (MXN)')
ax.set_title('Productos Navideños')

plt.xticks(rotation=45, ha='right')  

for bar, price in zip(bars, precios):
    ax.text(bar.get_x() + bar.get_width() / 2, bar.get_height(), f'{price}', 
            ha='center', va='bottom', fontsize=10)
    
plt.tight_layout()
plt.show()
