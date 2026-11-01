# junior-python-journey
Путь джуна в Python
import pandas as pd
import matplotlib.pyplot as plt

# Загрузка данных
df = pd.read_csv('city_lifestyle_dataset_2_fixed.csv')

# Группировка для линейного графика 
group = df.groupby('country')[['avg_income', 'avg_rent']].mean()

# Полотно
plt.figure(figsize=(15, 5))

#График 1: линейный (слева)
plt.subplot(1, 2, 1)

plt.plot(
    group.index,
    group['avg_income'],
    marker='o',
    color='green',
    label='Средний доход'
)
plt.plot(
    group.index,
    group['avg_rent'],
    marker='s',
    color='red',
    label='Средняя аренда'
)

plt.title('Средний доход и аренда по странам')
plt.xlabel('Страна')
plt.ylabel('Значение')
plt.legend(0
#Удалила параметр круговой диаграмы
plt.grid(True)
plt.title('Доля городов по диапазону плотности')
plt.tight_layout()
plt.show()
