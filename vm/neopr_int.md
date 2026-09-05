# Решения неопределённых интегралов

## 1. $$\int \left( \frac{1}{3\sqrt{x}} - \frac{x\sqrt[3]{x}}{5} + 1 \right) dx$$

Представим корни в виде степеней:  
$\sqrt{x} = x^{1/2}$, $\sqrt[3]{x} = x^{1/3}$, тогда $x\sqrt[3]{x} = x^{1+1/3} = x^{4/3}$.

Интеграл разбиваем на сумму:

$$\int \frac{1}{3} x^{-1/2} dx - \int \frac{1}{5} x^{4/3} dx + \int 1 dx$$

Используем табличную формулу $\int x^n dx = \frac{x^{n+1}}{n+1}$:

$$\frac{1}{3} \cdot \frac{x^{1/2}}{1/2} - \frac{1}{5} \cdot \frac{x^{7/3}}{7/3} + x + C = \frac{2}{3} x^{1/2} - \frac{3}{35} x^{7/3} + x + C$$

**Ответ:**  
$$\frac{2\sqrt{x}}{3} - \frac{3x^{7/3}}{35} + x + C$$

---

## 2. $$\int \left( \frac{2}{3+x^2} - \frac{1}{2\sqrt{x^2-3}} + 1 \right) dx$$

Интегрируем почленно:

$$\int \frac{2}{x^2+3} dx - \frac{1}{2} \int \frac{dx}{\sqrt{x^2-3}} + \int dx$$

1) $\int \frac{dx}{x^2+a^2} = \frac{1}{a} \arctan\frac{x}{a}$, здесь $a=\sqrt{3}$:  
   $$2 \cdot \frac{1}{\sqrt{3}} \arctan\frac{x}{\sqrt{3}} = \frac{2}{\sqrt{3}} \arctan\frac{x}{\sqrt{3}}$$

2) $\int \frac{dx}{\sqrt{x^2-a^2}} = \ln|x+\sqrt{x^2-a^2}|$, здесь $a=\sqrt{3}$:  
   $$-\frac{1}{2} \ln|x+\sqrt{x^2-3}|$$

3) $\int dx = x$

**Ответ:**  
$$\frac{2}{\sqrt{3}} \arctan\frac{x}{\sqrt{3}} - \frac{1}{2} \ln|x+\sqrt{x^2-3}| + x + C$$

---

## 3. $$\int \frac{\cot^3 x - 6}{\sin^2 x} dx$$

Разбиваем:

$$\int \frac{\cot^3 x}{\sin^2 x} dx - 6 \int \frac{dx}{\sin^2 x}$$

Заметим, что $d(\cot x) = -\frac{1}{\sin^2 x} dx$, значит $\frac{dx}{\sin^2 x} = -d(\cot x)$.

Тогда первый интеграл:  
$$\int \cot^3 x \cdot \frac{dx}{\sin^2 x} = \int \cot^3 x \cdot (-d(\cot x)) = -\int \cot^3 x \, d(\cot x) = -\frac{\cot^4 x}{4}$$

Второй интеграл:  
$$-6 \int \frac{dx}{\sin^2 x} = -6 \cdot (-\cot x) = 6 \cot x$$

**Ответ:**  
$$-\frac{\cot^4 x}{4} + 6\cot x + C$$

---

## 4. $$\int x(3x^2+1)^4 dx$$

Замена: $t = 3x^2+1$, тогда $dt = 6x\,dx$, откуда $x\,dx = \frac{dt}{6}$.

Интеграл принимает вид:

$$\int x(3x^2+1)^4 dx = \int t^4 \cdot \frac{dt}{6} = \frac{1}{6} \int t^4 dt = \frac{1}{6} \cdot \frac{t^5}{5} = \frac{t^5}{30}$$

Возвращаясь к $x$:

**Ответ:**  
$$\frac{(3x^2+1)^5}{30} + C$$

---

## 5. $$\int \frac{2x-1}{x^2+2x+10} dx$$

Знаменатель: $x^2+2x+10 = (x+1)^2 + 9$.

Производная знаменателя: $(x^2+2x+10)' = 2x+2$.  
Представим числитель: $2x-1 = (2x+2) - 3$.

Тогда интеграл:

$$\int \frac{2x+2}{x^2+2x+10} dx - 3 \int \frac{dx}{(x+1)^2+9}$$

Первый: $\int \frac{d(x^2+2x+10)}{x^2+2x+10} = \ln(x^2+2x+10)$ (без модуля, т.к. дискриминант отрицателен).

Второй: $\int \frac{dx}{(x+1)^2+3^2} = \frac{1}{3} \arctan\frac{x+1}{3}$.  
Умножаем на $3$: $3 \cdot \frac{1}{3} \arctan\frac{x+1}{3} = \arctan\frac{x+1}{3}$.

**Ответ:**  
$$\ln(x^2+2x+10) - \arctan\frac{x+1}{3} + C$$

---

## 6. $$\int \sqrt{1-e^x} \, e^x dx$$

Замена: $t = 1-e^x$, тогда $dt = -e^x dx$, значит $e^x dx = -dt$.

Интеграл:

$$\int \sqrt{t} \cdot (-dt) = -\int t^{1/2} dt = -\frac{2}{3} t^{3/2} + C$$

Возвращаемся:

**Ответ:**  
$$-\frac{2}{3} (1-e^x)^{3/2} + C$$

---

## 7. $$\int x \sin(2x) dx$$

Интегрируем по частям:  
$u = x$, $dv = \sin(2x) dx$, тогда $du = dx$, $v = -\frac{1}{2}\cos(2x)$.

По формуле $\int u dv = uv - \int v du$:

$$\int x \sin(2x) dx = -\frac{x}{2}\cos(2x) - \int \left(-\frac{1}{2}\cos(2x)\right) dx = -\frac{x}{2}\cos(2x) + \frac{1}{2} \int \cos(2x) dx$$

$$\int \cos(2x) dx = \frac{1}{2}\sin(2x)$$

Итог:

**Ответ:**  
$$-\frac{x}{2}\cos(2x) + \frac{1}{4}\sin(2x) + C$$

---

## 8. $$\int \frac{4x+3}{(x-2)^2} dx$$

Представим числитель через $(x-2)$:  
$4x+3 = 4(x-2) + 11$, т.к. $4(x-2)=4x-8$, и $+11$ даёт $4x+3$.

Тогда:

$$\int \left( \frac{4(x-2)}{(x-2)^2} + \frac{11}{(x-2)^2} \right) dx = \int \frac{4}{x-2} dx + 11 \int (x-2)^{-2} dx$$

Первый: $4\ln|x-2|$.  
Второй: $11 \cdot \frac{(x-2)^{-1}}{-1} = -\frac{11}{x-2}$.

**Ответ:**  
$$4\ln|x-2| - \frac{11}{x-2} + C$$

---

## 9. $$\int \frac{dx}{x(x^2+1)}$$

Разложим подынтегральную дробь на простейшие:

$$\frac{1}{x(x^2+1)} = \frac{A}{x} + \frac{Bx+C}{x^2+1}$$

Приводим к общему знаменателю:

$$1 = A(x^2+1) + (Bx+C)x = A x^2 + A + B x^2 + C x = (A+B)x^2 + C x + A$$

Сравниваем коэффициенты:  
$A+B=0$, $C=0$, $A=1$. Отсюда $B=-1$.

Таким образом:

$$\frac{1}{x(x^2+1)} = \frac{1}{x} - \frac{x}{x^2+1}$$

Интегрируем:

$$\int \frac{dx}{x} - \int \frac{x}{x^2+1} dx = \ln|x| - \frac{1}{2}\ln(x^2+1) + C$$

Можно объединить логарифмы:

$$\ln|x| - \frac{1}{2}\ln(x^2+1) = \ln\frac{|x|}{\sqrt{x^2+1}}$$

**Ответ:**  
$$\ln\frac{|x|}{\sqrt{x^2+1}} + C$$

---

## 10. $$\int \frac{dx}{\sqrt{x} + \sqrt[3]{x} + 2\sqrt[4]{x}}$$

Сделаем замену: $x = t^{12}$, где $12 = \text{НОК}(2,3,4)$.  
Тогда $dx = 12 t^{11} dt$,  
$\sqrt{x} = t^6$,  
$\sqrt[3]{x} = t^4$,  
$\sqrt[4]{x} = t^3$.

Подставляем:

$$\int \frac{12 t^{11} dt}{t^6 + t^4 + 2 t^3} = 12 \int \frac{t^{11}}{t^3(t^3 + t + 2)} dt = 12 \int \frac{t^8}{t^3 + t + 2} dt$$

Делим многочлен $t^8$ на $t^3 + t + 2$:

$$\frac{t^8}{t^3+t+2} = t^5 - t^3 - 2t^2 + t + 4 + \frac{3t^2 - 6t - 8}{t^3+t+2}$$

Теперь разложим дробь $\frac{3t^2 - 6t - 8}{t^3+t+2}$. Заметим, что $t^3+t+2 = (t+1)(t^2 - t + 2)$, так как $-1$ — корень.

$$\frac{3t^2 - 6t - 8}{(t+1)(t^2 - t + 2)} = \frac{A}{t+1} + \frac{Bt+C}{t^2 - t + 2}$$

Находим $A, B, C$:

$$3t^2 - 6t - 8 = A(t^2 - t + 2) + (Bt+C)(t+1)$$

Раскрываем:  
$A t^2 - A t + 2A + B t^2 + B t + C t + C = (A+B)t^2 + (-A+B+C)t + (2A+C)$

Сравниваем:

$$\begin{cases} A+B = 3 \\ -A+B+C = -6 \\ 2A+C = -8 \end{cases}$$

Из первого $B = 3 - A$.  
Подставляем во второе: $-A + (3-A) + C = -6 \Rightarrow -2A + 3 + C = -6 \Rightarrow C = -9 + 2A$.  
В третье: $2A + (-9+2A) = -8 \Rightarrow 4A - 9 = -8 \Rightarrow 4A = 1 \Rightarrow A = \frac{1}{4}$.  
Тогда $B = 3 - \frac{1}{4} = \frac{11}{4}$, $C = -9 + \frac{1}{2} = -\frac{17}{2}$.

Итак, дробь:

$$\frac{1}{4} \cdot \frac{1}{t+1} + \frac{\frac{11}{4}t - \frac{17}{2}}{t^2 - t + 2}$$

Теперь интегрируем:

$$\int \frac{3t^2 - 6t - 8}{t^3+t+2} dt = \frac{1}{4} \ln|t+1| + \int \frac{\frac{11}{4}t - \frac{17}{2}}{t^2 - t + 2} dt$$

Выделим в числителе производную знаменателя $(t^2 - t + 2)' = 2t - 1$:

$$\frac{11}{4}t - \frac{17}{2} = \frac{11}{8}(2t) - \frac{17}{2} = \frac{11}{8}(2t - 1) + \left( \frac{11}{8} - \frac{17}{2} \right) = \frac{11}{8}(2t - 1) - \frac{57}{8}$$

Тогда:

$$\int \frac{\frac{11}{4}t - \frac{17}{2}}{t^2 - t + 2} dt = \frac{11}{8} \int \frac{2t-1}{t^2 - t + 2} dt - \frac{57}{8} \int \frac{dt}{t^2 - t + 2}$$

Первый интеграл: $\frac{11}{8} \ln|t^2 - t + 2|$.  
Второй: $t^2 - t + 2 = (t - \frac{1}{2})^2 + \frac{7}{4} = (t - \frac{1}{2})^2 + \left(\frac{\sqrt{7}}{2}\right)^2$,  
$$\int \frac{dt}{t^2 - t + 2} = \frac{2}{\sqrt{7}} \arctan\frac{2t-1}{\sqrt{7}}$$

Следовательно, интеграл от дроби:

$$\frac{1}{4} \ln|t+1| + \frac{11}{8} \ln|t^2 - t + 2| - \frac{57}{8} \cdot \frac{2}{\sqrt{7}} \arctan\frac{2t-1}{\sqrt{7}} =$$

$$= \frac{1}{4} \ln|t+1| + \frac{11}{8} \ln|t^2 - t + 2| - \frac{57}{4\sqrt{7}} \arctan\frac{2t-1}{\sqrt{7}}$$

Теперь вспоминаем множитель $12$ перед интегралом и добавляем интеграл от многочлена $t^5 - t^3 - 2t^2 + t + 4$:

$$\int (t^5 - t^3 - 2t^2 + t + 4) dt = \frac{t^6}{6} - \frac{t^4}{4} - \frac{2t^3}{3} + \frac{t^2}{2} + 4t$$

Умножаем всё на $12$:

$$12 \left( \frac{t^6}{6} - \frac{t^4}{4} - \frac{2t^3}{3} + \frac{t^2}{2} + 4t \right) = 2t^6 - 3t^4 - 8t^3 + 6t^2 + 48t$$

Для дробной части:

$$12 \left( \frac{1}{4} \ln|t+1| + \frac{11}{8} \ln|t^2 - t + 2| - \frac{57}{4\sqrt{7}} \arctan\frac{2t-1}{\sqrt{7}} \right) =$$

$$= 3 \ln|t+1| + \frac{33}{2} \ln|t^2 - t + 2| - \frac{171}{\sqrt{7}} \arctan\frac{2t-1}{\sqrt{7}}$$

Осталось вернуться к $x = t^{12}$, т.е. $t = x^{1/12}$.

**Ответ:**  
$$2x^{1/2} - 3x^{1/3} - 8x^{1/4} + 6x^{1/6} + 48x^{1/12} + 3\ln|x^{1/12}+1| + \frac{33}{2}\ln|x^{1/6} - x^{1/12} + 2| - \frac{171}{\sqrt{7}} \arctan\frac{2x^{1/12}-1}{\sqrt{7}} + C$$

где $C$ — произвольная постоянная.
