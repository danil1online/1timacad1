# Решения задач по дифференциальным уравнениям

---

## Задание 1. Найти общий интеграл или общее решение ДУ первого порядка

### 1) $$\sqrt{4-x^2}y' + xy^2 + x = 0$$

Разделяем переменные:

$$\sqrt{4-x^2}y' = -x(y^2+1) \quad \Rightarrow \quad \frac{dy}{y^2+1} = -\frac{x}{\sqrt{4-x^2}}dx$$

Интегрируем:

$$\int \frac{dy}{y^2+1} = -\int \frac{x\,dx}{\sqrt{4-x^2}}$$

Левый интеграл: $\arctan y$.  
Правый: замена $t=4-x^2$, тогда $x dx = -dt/2$, получаем $\sqrt{4-x^2}+C$.

$$\arctan y = \sqrt{4-x^2}+C \quad \Rightarrow \quad y = \tan\left(\sqrt{4-x^2}+C\right)$$

**Ответ:** $$y = \tan\left(\sqrt{4-x^2}+C\right)$$

---

### 2) $$20x\,dx - 3y\,dy = 3x^2 y\,dy - 5x y^2\,dx$$

Перенесём все в одну сторону и сгруппируем:

$$(20x + 5xy^2)dx - (3y + 3x^2 y)dy = 0$$

$$5x(4+y^2)dx - 3y(1+x^2)dy = 0$$

Разделяем переменные:

$$\frac{5x}{1+x^2}dx = \frac{3y}{4+y^2}dy$$

Интегрируем:

$$\frac{5}{2}\ln(1+x^2) = \frac{3}{2}\ln(4+y^2) + C$$

Умножаем на 2 и потенцируем:

$$(1+x^2)^5 = C(4+y^2)^3$$

**Ответ:** $$(1+x^2)^5 = C(4+y^2)^3$$

---

### 3) $$y' = \frac{x^2+2xy-5y^2}{2x^2-6xy}$$

Правая часть однородная. Замена $y = xu$, $y' = u + xu'$.

$$u + xu' = \frac{1+2u-5u^2}{2-6u}$$

$$xu' = \frac{1+2u-5u^2}{2-6u} - u = \frac{1+u^2}{2-6u}$$

Разделяем:

$$\frac{2-6u}{1+u^2}du = \frac{dx}{x}$$

Интегрируем:

$$2\arctan u - 3\ln(1+u^2) = \ln|x| + C$$

Возвращаем $u = y/x$:

$$2\arctan\frac{y}{x} - 3\ln\left(1+\frac{y^2}{x^2}\right) = \ln|x| + C$$

Упрощаем до:

$$2\arctan\frac{y}{x} + \ln\frac{|x|^5}{(x^2+y^2)^3} = C$$

**Ответ:** $$2\arctan\frac{y}{x} + \ln\frac{|x|^5}{(x^2+y^2)^3} = C$$

---

### 4) Задача Коши: $$y' - y\cos x = \sin 2x,\quad y(0) = -1$$

Линейное уравнение. Интегрирующий множитель:

$$\mu = e^{-\int \cos x\,dx} = e^{-\sin x}$$

Умножаем:

$$(y e^{-\sin x})' = e^{-\sin x}\sin 2x$$

Интегрируем: $\int e^{-\sin x}\sin 2x\,dx = -2e^{-\sin x}(\sin x + 1)$ (замена $t=\sin x$).

$$y e^{-\sin x} = -2e^{-\sin x}(\sin x+1) + C$$

$$y = -2(\sin x+1) + Ce^{\sin x}$$

Из $y(0)=-1$: $-1 = -2 + C \Rightarrow C=1$.

**Ответ:** $$y = -2(\sin x+1) + e^{\sin x}$$

---

### 5) Задача Коши: $$x y' + y = x y^2,\quad y(1)=1$$

Уравнение Бернулли. Разделим на $y^2$:

$$x y^{-2}y' + y^{-1} = x$$

Замена $z = y^{-1}$, тогда $z' = -y^{-2}y'$, получаем:

$$-x z' + z = x \quad \Rightarrow \quad z' - \frac{1}{x}z = -1$$

Интегрирующий множитель $\mu = e^{-\ln x} = \frac{1}{x}$:

$$\left(\frac{z}{x}\right)' = -\frac{1}{x} \quad \Rightarrow \quad \frac{z}{x} = -\ln|x| + C$$

$$z = x(C - \ln|x|) \quad \Rightarrow \quad y = \frac{1}{x(C - \ln|x|)}$$

Из $y(1)=1$: $1 = \frac{1}{C} \Rightarrow C=1$.

**Ответ:** $$y = \frac{1}{x(1-\ln x)}$$

---

### 6) $$\frac{y}{x^2}dx - \frac{xy+1}{x}dy = 0$$

Приводим к виду:

$$\frac{y}{x^2}dx - \left(y + \frac{1}{x}\right)dy = 0$$

Проверяем условие полного дифференциала:

$$M = \frac{y}{x^2}, \quad N = -y - \frac{1}{x}$$

$$\frac{\partial M}{\partial y} = \frac{1}{x^2}, \quad \frac{\partial N}{\partial x} = \frac{1}{x^2}$$

Равны, значит это уравнение в полных дифференциалах. Находим $U$:

$$U_x = \frac{y}{x^2} \Rightarrow U = -\frac{y}{x} + \varphi(y)$$

$$U_y = -\frac{1}{x} + \varphi'(y) = -y - \frac{1}{x} \Rightarrow \varphi'(y) = -y \Rightarrow \varphi(y) = -\frac{y^2}{2}$$

$$U = -\frac{y}{x} - \frac{y^2}{2} = C$$

**Ответ:** $$\frac{y}{x} + \frac{y^2}{2} = C$$

---

## Задание 2. Найти общее решение ДУ высших порядков

### 1) $$y''' x \ln x = y''$$

Обозначим $p = y''$, тогда $p' = y'''$:

$$x \ln x \cdot p' = p \quad \Rightarrow \quad \frac{dp}{p} = \frac{dx}{x\ln x}$$

Интегрируем:

$$\ln|p| = \ln|\ln x| + C_1 \Rightarrow p = C_1 \ln x$$

То есть $y'' = C_1 \ln x$. Интегрируем дважды:

$$y' = C_1(x\ln x - x) + C_2$$

$$y = C_1\left(\frac{x^2}{2}\ln x - \frac{3x^2}{4}\right) + C_2 x + C_3$$

**Ответ:** $$y = C_1\left(\frac{x^2}{2}\ln x - \frac{3x^2}{4}\right) + C_2 x + C_3$$

---

### 2) $$(1+x^2)y'' + 2xy' = 12x^2$$

Заметим, что левая часть есть $\left((1+x^2)y'\right)'$:

$$\left((1+x^2)y'\right)' = 12x^2$$

Интегрируем:

$$(1+x^2)y' = 4x^3 + C_1$$

$$y' = \frac{4x^3 + C_1}{1+x^2} = \frac{4x^3}{1+x^2} + \frac{C_1}{1+x^2}$$

Интегрируем:

$$y = \int \frac{4x^3}{1+x^2} dx + C_1 \int \frac{dx}{1+x^2} + C_2$$

$$\int \frac{4x^3}{1+x^2} dx = 4\int \left(x - \frac{x}{1+x^2}\right) dx = 2x^2 - 2\ln(1+x^2)$$

$$\int \frac{dx}{1+x^2} = \arctan x$$

**Ответ:** $$y = 2x^2 - 2\ln(1+x^2) + C_1\arctan x + C_2$$

---

## Задание 3. Решить задачу Коши

$$\begin{cases} y'' = 2\sin^3 y \cos y \\ y(1)=\frac{\pi}{2}, \quad y'(1)=1 \end{cases}$$

Уравнение не содержит $x$. Замена $p = y'$, тогда $y'' = p \frac{dp}{dy}$.

$$p \frac{dp}{dy} = 2\sin^3 y \cos y$$

$$p\,dp = 2\sin^3 y \cos y\,dy$$

Интегрируем:

$$\frac{p^2}{2} = 2 \cdot \frac{\sin^4 y}{4} + C_1 = \frac{\sin^4 y}{2} + C_1$$

$$p^2 = \sin^4 y + C_2$$

При $x=1$: $y=\pi/2$, $p=1$. Тогда $1^2 = 1 + C_2 \Rightarrow C_2 = 0$.

$$p^2 = \sin^4 y \Rightarrow p = \pm \sin^2 y$$

Так как $p(1)=1>0$, берём $p = \sin^2 y$.

$$\frac{dy}{dx} = \sin^2 y \Rightarrow \frac{dy}{\sin^2 y} = dx$$

Интегрируем:

$$-\cot y = x + C_3$$

При $x=1$, $y=\pi/2$: $-\cot(\pi/2)=0 = 1 + C_3 \Rightarrow C_3 = -1$.

$$-\cot y = x - 1 \Rightarrow \cot y = 1 - x$$

**Ответ:** $$y = \arccot (1-x)$$

---

## Задание 4. Найти общее решение ЛНДУ (в примере 6 – задачу Коши)

### 1) $$y'' - 2y' + y = x e^x$$

Характеристическое: $k^2 - 2k + 1 = (k-1)^2 = 0$, корень $k=1$ кратности 2.

Однородное: $y_{одн} = (C_1 + C_2 x)e^x$.

Частное решение ищем в виде $y_{ч} = x^2(Ax + B)e^x$ (кратность 2).  
Подстановка даёт $A = \frac{1}{6}$, $B = 0$.

$$y_{ч} = \frac{1}{6}x^3 e^x$$

**Ответ:** $$y = e^x\left(C_1 + C_2 x + \frac{x^3}{6}\right)$$

---

### 2) $$y'' + 4y' + 5y = x^2$$

Характеристическое: $k^2+4k+5=0$, корни $k = -2 \pm i$.  
$y_{одн} = e^{-2x}(C_1\cos x + C_2\sin x)$.

Частное решение: $y_{ч} = Ax^2 + Bx + C$.  
Подстановка даёт: $A = \frac{1}{5}$, $B = -\frac{8}{25}$, $C = \frac{22}{125}$.

**Ответ:** $$y = e^{-2x}(C_1\cos x + C_2\sin x) + \frac{1}{5}x^2 - \frac{8}{25}x + \frac{22}{125}$$

---

### 3) $$y''' - 4y'' + 5y' = 6x^2 + 2x - 5$$

Характеристическое: $k(k^2-4k+5)=0$ → $k=0$, $k=2\pm i$.

$y_{одн} = C_1 + e^{2x}(C_2\cos x + C_3\sin x)$.

Частное решение: $y_{ч} = x(Ax^2+Bx+C)$ (так как $k=0$ – простой корень).  
Подстановка: $A = \frac{2}{5}$, $B = \frac{29}{25}$, $C = \frac{47}{125}$.

**Ответ:** $$y = C_1 + e^{2x}(C_2\cos x + C_3\sin x) + \frac{2}{5}x^3 + \frac{29}{25}x^2 + \frac{47}{125}x$$

---

### 4) $$y'' - 4y' + 4y = e^{2x}(\cos x + 3\sin x)$$

Характеристическое: $(k-2)^2=0$ → корень $k=2$ кратности 2.

$y_{одн} = (C_1 + C_2 x)e^{2x}$.

Частное решение: $y_{ч} = e^{2x}(A\cos x + B\sin x)$.  
Подстановка: $A = -1$, $B = -3$.

$$y_{ч} = -e^{2x}(\cos x + 3\sin x)$$

**Ответ:** $$y = e^{2x}(C_1 + C_2 x - \cos x - 3\sin x)$$

---

### 5) $$y''' - 64y' = 128\cos 8x - 64e^{8x}$$

Характеристическое: $k(k-8)(k+8)=0$ → корни $0, 8, -8$.

$y_{одн} = C_1 + C_2 e^{8x} + C_3 e^{-8x}$.

Для $\cos 8x$: частное $y_{ч1} = A\cos 8x + B\sin 8x$.  
Подстановка: $A=0$, $B=-\frac{1}{8}$.

Для $-64e^{8x}$: так как $k=8$ – простой корень, $y_{ч2} = C x e^{8x}$.  
Подстановка: $C = -\frac{1}{2}$.

**Ответ:** $$y = C_1 + C_2 e^{8x} + C_3 e^{-8x} - \frac{1}{8}\sin 8x - \frac{1}{2}x e^{8x}$$

---

### 6) Задача Коши: $$y'' + y = \frac{1}{\sin x},\quad y\left(\frac{\pi}{2}\right)=1,\; y'\left(\frac{\pi}{2}\right)=\frac{\pi}{2}$$

Однородное: $y_{одн} = C_1\cos x + C_2\sin x$.

Метод вариации: $y_{ч} = u_1 \cos x + u_2 \sin x$.

Система для $u_1', u_2'$:

$$\begin{cases} u_1'\cos x + u_2'\sin x = 0 \\ -u_1'\sin x + u_2'\cos x = \frac{1}{\sin x} \end{cases}$$

Решение: $u_1' = -1$, $u_2' = \cot x$.  
$u_1 = -x$, $u_2 = \ln|\sin x|$.

$$y_{ч} = -x\cos x + \sin x \ln|\sin x|$$

Общее решение:

$$y = C_1\cos x + C_2\sin x - x\cos x + \sin x \ln|\sin x|$$

Из условий: $y(\pi/2)=1$ → $C_2=1$.  
$y'(\pi/2) = \pi/2$ → $-C_1 + \frac{\pi}{2} = \frac{\pi}{2}$ → $C_1=0$.

**Ответ:** $$y = \sin x - x\cos x + \sin x \ln(\sin x)$$
