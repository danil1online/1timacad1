# Решения задач по функциям нескольких переменных

---

## 1. Область определения функции

$$z = \frac{\ln(1 - x^2 - y^2)}{1 - \sqrt{y}}$$

**Условия:**
1. Логарифм определён: $1 - x^2 - y^2 > 0 \;\Rightarrow\; x^2 + y^2 < 1$.
2. Знаменатель не равен нулю: $1 - \sqrt{y} \neq 0 \;\Rightarrow\; \sqrt{y} \neq 1 \;\Rightarrow\; y \neq 1$.
3. Корень $\sqrt{y}$ определён: $y \ge 0$.

Но при $y = 1$ неравенство $x^2 + 1 < 1$ невыполнимо (так как $x^2 \ge 0$), поэтому условие $y \neq 1$ автоматически следует из $x^2 + y^2 < 1$.

**Область определения:**

$$D = \left\\{ (x, y) \mid x^2 + y^2 < 1, \; y \ge 0 \right\\}$$ 

---

## 2. Частные производные в заданных точках

### а) $z = x^{1/y}$, точка $(1; 1)$

Найдём частные производные:

$$\frac{\partial z}{\partial x} = \frac{1}{y} x^{1/y - 1}, \qquad \frac{\partial z}{\partial y} = -\frac{\ln x}{y^2} x^{1/y}$$

В точке $(1, 1)$:

$$\frac{\partial z}{\partial x}(1,1) = \frac{1}{1} \cdot 1^{0} = 1$$

$$\frac{\partial z}{\partial y}(1,1) = -\frac{\ln 1}{1} \cdot 1 = 0$$

**Ответ:**  
$$\frac{\partial z}{\partial x}(1,1) = 1, \qquad \frac{\partial z}{\partial y}(1,1) = 0$$

---

### б) $z = \ln\left(\sqrt{x} + \sqrt{y}\right)$, точка $(1; 1)$

$$\frac{\partial z}{\partial x} = \frac{1}{\sqrt{x}+\sqrt{y}} \cdot \frac{1}{2\sqrt{x}} = \frac{1}{2\sqrt{x}(\sqrt{x}+\sqrt{y})}$$

$$\frac{\partial z}{\partial y} = \frac{1}{2\sqrt{y}(\sqrt{x}+\sqrt{y})}$$

В точке $(1, 1)$:

$$\frac{\partial z}{\partial x}(1,1) = \frac{1}{2 \cdot 1 \cdot (1+1)} = \frac{1}{4}$$

$$\frac{\partial z}{\partial y}(1,1) = \frac{1}{4}$$

**Ответ:**  
$$\frac{\partial z}{\partial x}(1,1) = \frac{1}{4}, \qquad \frac{\partial z}{\partial y}(1,1) = \frac{1}{4}$$

---

## 3. Вторая производная $\frac{\partial^2 u}{\partial x^2}$ для $u = xy + \sin(x+y)$

Первая производная по $x$:

$$\frac{\partial u}{\partial x} = y + \cos(x+y)$$

Вторая производная:

$$\frac{\partial^2 u}{\partial x^2} = -\sin(x+y)$$

**Ответ:**  
$$\frac{\partial^2 u}{\partial x^2} = -\sin(x+y)$$

---

## 4. Экстремумы функции $z = x^2 + 2y^2 - 4x - 6y + 2$

Находим стационарные точки:

$$\frac{\partial z}{\partial x} = 2x - 4 = 0 \;\Rightarrow\; x = 2$$

$$\frac{\partial z}{\partial y} = 4y - 6 = 0 \;\Rightarrow\; y = \frac{3}{2}$$

Вторые производные:

$$z''_{xx} = 2, \qquad z''_{yy} = 4, \qquad z''_{xy} = 0$$

$$\Delta = z''_{xx} \cdot z''_{yy} - (z''_{xy})^2 = 2 \cdot 4 - 0 = 8 > 0$$

Так как $z''_{xx} = 2 > 0$, в точке $(2, \frac{3}{2})$ – **минимум**.

Значение функции:

$$z(2, \frac{3}{2}) = 4 + 2 \cdot \frac{9}{4} - 8 - 9 + 2 = 4 + \frac{9}{2} - 15 = \frac{8}{2} + \frac{9}{2} - \frac{30}{2} = -\frac{13}{2}$$

**Ответ:**  
Точка минимума $\left(2, \frac{3}{2}\right)$, значение $z_{\min} = -\frac{13}{2}$.

---

## 5. Производная функции $z = \frac{\ln x}{y} - \frac{\ln y}{x}$ в направлении вектора $(1;1)$

(Вычисляем в точке $(1,1)$, так как точка не указана явно, но обычно подразумевается.)

Градиент:

$$\frac{\partial z}{\partial x} = \frac{1}{xy} + \frac{\ln y}{x^2}, \qquad \frac{\partial z}{\partial y} = -\frac{\ln x}{y^2} - \frac{1}{xy}$$

В точке $(1,1)$:

$$\frac{\partial z}{\partial x}(1,1) = 1 + 0 = 1, \qquad \frac{\partial z}{\partial y}(1,1) = 0 - 1 = -1$$

$$\nabla z(1,1) = (1, -1)$$

Единичный вектор направления $\vec{l} = (1,1)$: $|\vec{l}| = \sqrt{2}$, $\vec{l}_0 = \left(\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}\right)$.

Производная по направлению:

$$\frac{\partial z}{\partial \vec{l}} = \nabla z \cdot \vec{l}_0 = 1 \cdot \frac{1}{\sqrt{2}} + (-1) \cdot \frac{1}{\sqrt{2}} = 0$$

**Ответ:**  
$$\frac{\partial z}{\partial \vec{l}}(1,1) = 0$$

---

## 6. Экстремальное значение $z = 2x - y - y^2 - x^2$ при условии $x + 2y = 1$

Выразим $x = 1 - 2y$ и подставим:

$$z(y) = 2(1-2y) - y - y^2 - (1-2y)^2 = 2 - 4y - y - y^2 - (1 - 4y + 4y^2)$$

$$= 2 - 5y - y^2 - 1 + 4y - 4y^2 = 1 - y - 5y^2$$

Это парабола, ветви вниз. Вершина:

$$y = -\frac{b}{2a} = -\frac{-1}{2 \cdot (-5)} = -\frac{1}{10}$$

$$x = 1 - 2\left(-\frac{1}{10}\right) = 1 + \frac{1}{5} = \frac{6}{5}$$

Максимальное значение:

$$z_{\max} = 1 - \left(-\frac{1}{10}\right) - 5\left(\frac{1}{100}\right) = 1 + \frac{1}{10} - \frac{1}{20} = 1 + \frac{2}{20} - \frac{1}{20} = 1 + \frac{1}{20} = \frac{21}{20}$$

**Ответ:**  
$$z_{\max} = \frac{21}{20}$$

---

## 7. Вычисление повторного интеграла

$$\int_{-2}^{2} dy \int_{0}^{y^2} (2x + y) \, dx$$

Внутренний интеграл:

$$\int_{0}^{y^2} (2x + y) dx = \left[ x^2 + yx \right]_{0}^{y^2} = y^4 + y^3$$

Внешний интеграл:

$$\int_{-2}^{2} (y^4 + y^3) dy = \int_{-2}^{2} y^4 dy + \int_{-2}^{2} y^3 dy$$

$y^3$ — нечётная, интеграл по симметричному промежутку равен $0$.

$$\int_{-2}^{2} y^4 dy = 2 \int_{0}^{2} y^4 dy = 2 \cdot \frac{2^5}{5} = 2 \cdot \frac{32}{5} = \frac{64}{5}$$

**Ответ:**  
$$\frac{64}{5}$$

---

## 8. Изменение порядка интегрирования

Дан интеграл:

$$\int_{1}^{4} dy \int_{1/y}^{\frac{2}{3}y + \frac{1}{3}} f(x, y) \, dx$$

Область: $1 \le y \le 4$, $\frac{1}{y} \le x \le \frac{2y+1}{3}$.

Найдём границы по $x$:

- При $y=1$: $x=1$ (обе кривые дают 1).
- При $y=4$: нижняя $x=\frac{1}{4}$, верхняя $x=3$.
- Кривые пересекаются только в $(1,1)$.

Разбиваем область на две части по $x$:

**Для $x \in \left[\frac{1}{4}, 1\right]$:**  
нижняя граница по $y$: $y = \frac{1}{x}$ (из $x = \frac{1}{y}$), верхняя: $y = 4$.

**Для $x \in [1, 3]$:**  
нижняя граница: $y = \frac{3x-1}{2}$ (из $x = \frac{2y+1}{3}$), верхняя: $y = 4$.

Таким образом, новый порядок:

$$\int_{1/4}^{1} dx \int_{1/x}^{4} f(x,y) \, dy \;+\; \int_{1}^{3} dx \int_{(3x-1)/2}^{4} f(x,y) \, dy$$

**Ответ:**  
$$\int_{1/4}^{1} dx \int_{1/x}^{4} f \, dy \;+\; \int_{1}^{3} dx \int_{(3x-1)/2}^{4} f \, dy$$

---

## 9. Вычисление двойного интеграла

$$\iint_{D} \frac{x^2}{y^2} \, dxdy, \quad D:\; y = \frac{1}{x},\; y = x,\; x = 4$$

Область: $1 \le x \le 4$, $\frac{1}{x} \le y \le x$.

Интеграл:

$$\int_{1}^{4} dx \int_{1/x}^{x} \frac{x^2}{y^2} \, dy = \int_{1}^{4} x^2 \left[ -\frac{1}{y} \right]_{1/x}^{x} dx = \int_{1}^{4} x^2 \left( -\frac{1}{x} + \frac{1}{1/x} \right) dx$$

$$= \int_{1}^{4} x^2 \left( -\frac{1}{x} + x \right) dx = \int_{1}^{4} (-x + x^3) dx = \int_{1}^{4} (x^3 - x) dx$$

$$= \left[ \frac{x^4}{4} - \frac{x^2}{2} \right]_{1}^{4} = \left( \frac{256}{4} - \frac{16}{2} \right) - \left( \frac{1}{4} - \frac{1}{2} \right)$$

$$= (64 - 8) - \left( \frac{1}{4} - \frac{2}{4} \right) = 56 - \left( -\frac{1}{4} \right) = 56 + \frac{1}{4} = \frac{225}{4}$$

**Ответ:**  
$$\frac{225}{4}$$
