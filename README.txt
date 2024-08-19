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
