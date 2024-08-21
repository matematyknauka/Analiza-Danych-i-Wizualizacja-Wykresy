Komórka Colab

import numpy as np
import matplotlib.pyplot as plt

# Generowanie danych x i y z krokiem 0.01
x = np.arange(-np.pi, np.pi, 0.01)  # Tworzenie wektora x od ... do ... z krokiem 0.01
y = np.sin(x)  # Obliczanie wartości funkcji sinus dla wektora x

# Tworzenie wykresu
plt.figure(figsize=(10, 6))  # Ustawienie rozmiaru figury
plt.plot(x, y)  # Rysowanie wykresu funkcji sinus
plt.title('Wykres funkcji sinus')  # Dodanie tytułu wykresu
plt.xlabel('Oś x')  # Dodanie etykiety osi x
plt.ylabel('Oś y')  # Dodanie etykiety osi y
plt.grid(True)  # Dodanie siatki na wykresie
plt.axhline(0, color='black', lw=0.5, ls='--')  # Dodanie linii poziomej na poziomie 0
plt.axvline(0, color='black', lw=0.5, ls='--')  # Dodanie linii pionowej na poziomie 0
plt.show()  # Wyświetlenie wykresu

Koniec komórki

Komórka

import pandas as pd
import matplotlib.pyplot as plt
df = pd.DataFrame({'ID_ucznia': [0, 1, 2, 3, 4], 'Oceny': [5, 4, 3, 2, 5], 'Wiek': [15, 16, 17, 15, 16]})
df.to_csv('uczniowie.csv', index=False)
csv_read = pd.read_csv('uczniowie.csv')
plt.figure(figsize=(8, 6))
plt.hist(csv_read['Oceny'], bins=5) # Sprawdzić to jeszcze: Przedział P: [ocena min, ocena max] dzielę na przedziały o długości przedziału P/bins chyba [) i na końcu []
plt.xlabel('Oceny')
plt.ylabel('Liczba uczniów')
plt.title('Histogram ocen uczniów')
plt.show()
Koniec komórki

Komórka

import pandas as pd
import matplotlib.pyplot as plt

data = {'A':[5, 4, 3, 2, 1], 'B':[6, 7, 8, 9, 10]}
df = pd.DataFrame(data)

wartosci, bins, bar = plt.hist(df['A'], bins = 2) # zmmienna = plt.hist(df['A'], bins = 2) to tablica. wartosci to zerowy element, bins pierwszy itd...
plt.title('Histogram')
plt.xlabel('x')
plt.ylabel('y')
plt.xticks(bins) # bins - lista końców/początków przedziałów
plt.yticks([0, 1, 2, 3, 4])
plt.show()

Koniec komórki
