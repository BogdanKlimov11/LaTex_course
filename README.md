<h1 id="top">Справочник по системе компьютерной верстки LaTex</h1>

<img src="https://github.com/BogdanKlimov11/LaTex_course/assets/136115919/68fa1820-2de8-411a-bd41-5c8e8975adec" alt="LaTex logo" title="LaTex" width="100%" height="auto">

---

<!-- Table of Contents -->
<h3>Table of Contents</h3>
<nav>
    <ol>
        <li><a href="#general">Общие (General)</a></li>
        <ul>
            <li><a href="#degrees-indices">Степени и индексы (Degrees and Indices)</a></li>
            <li><a href="#color">Цвет (Color)</a></li>
            <li><a href="#fractions-binomials">Дроби и биномы (Fractions and Binomials)</a></li>
            <li><a href="#roots">Корни (Roots)</a></li>
            <li><a href="#parentheses-separators">Скобки и разделители (Parentheses and Separators)</a></li>
            <li><a href="#limits">Пределы (Limits)</a></li>
        </ul>
        <li><a href="#series-integrals">Ряды и интегралы (Series and Integrals)</a></li>
    	<li><a href="#relation-symbols">Символы отношений (Relation Symbols)</a></li>
        <li><a href="#binary-operations">Бинарные операции (Binary Operations)</a></li>
        <li><a href="#logic-notation">Обозначение набора и/или логики (Set and/or Logic Notation)</a></li>
        <li><a href="#delimiters">Разделители (Delimiters)</a></li>
        <li><a href="#greek-letters">Греческие буквы (Greek Letters)</a></li>
        <li><a href="#other-symbols">Другие символы (Other Symbols)</a></li>
        <li><a href="#trigonometric-functions">Тригонометрические функции (Trigonometric Functions)</a></li>
        <li><a href="#dots">Точки (Dots)</a></li>
        <li><a href="#accents">Акценты (Accents)</a></li>
        <li><a href="#fonts">Шрифты (Fonts)</a></li>
        <li><a href="#matrices-arrays">Матрицы и массивы (Matrices and Arrays)</a></li>
    </ol>
</nav>

---

<!-- General -->
<h4 id="general">Общие (General) <a href="#top">↑top↑</a></h4>

В математике существует достаточно много различных символов! Ниже приведены те, к которым можно получить доступ прямо с клавиатуры:

```latex
+ - = ! / ( ) [ ] < > | ' : *
```

<!-- Degrees and indices -->
<h5 id="degrees-indices">Степени и индексы (Degrees and Indices) <a href="#top">↑top↑</a></h5>

Степени и индексы эквивалентны верхним и нижним индексам в обычном текстовом режиме. Символ каретки (`^`; так же известный как циркумфлекс) 
используется чтобы что-то поднять, а нижнее подчёркивание (`_`) для опускания. Если необходимо повысить или понизить выражение, содержащее 
больше одного символа, его необходимо сгруппировать с помощью фигурных скобок ({ и }).

<table>
    <tr>
        <td>$k_{n+1} = n^2 + k_n^2 - k_{n-1}$</td>
        <td><code>k_{n+1} = n^2 + k_n^2 - k_{n-1}</code></td>
    </tr>
</table>

Для степеней, состоящих из более чем одной цифры, заключите степень в `{}`.

<table>
    <tr>
        <td>$n^{22}$</td>
        <td><code>n^{22}</code></td>
    </tr>
</table>

Подчёркивание (`_`) может использоваться с вертикальной чертой (`|`) при использовании выражения в качестве нижнего индекса.

<table>
    <tr>
        <td>$f(n) = n^5 + 4n^2 + 2 |_{n=17}$</td>
        <td><code>f(n) = n^5 + 4n^2 + 2 |_{n=17}</code></td>
    </tr>
</table>

<!-- Color -->
<h5 id="color">Цвет (Color) <a href="#top">↑top↑</a></h5>

В формулах можно изменять цвет символов.

<table>
    <tr>
        <td>$k = {\color{red}x} \mathbin{\color{blue}-} 2$</td>
        <td><code>k = {\color{red}x} \mathbin{\color{blue}-} 2</code></td>
    </tr>
</table>

<!-- Fractions and binomials -->
<h5 id="fractions-binomials">Дроби и биномы (Fractions and Binomials) <a href="#top">↑top↑</a></h5>

Дроби создаются с помощью команды `\frac{numerator}{denominator}`. Так же и Биномиальный коэффициент можно записать используя команду `\binom`.

<table>
    <tr>
        <td>$\frac{n!}{k!(n-k)!} = \binom{n}{k}$</td>
        <td><code>\frac{n!}{k!(n-k)!} = \binom{n}{k}</code></td>
    </tr>
</table>

Дроби можно помещать одну внутри другой.

<table>
    <tr>
        <td>$\frac{\frac{1}{x}+\frac{1}{y}}{y-z}$</td>
        <td><code>\frac{\frac{1}{x}+\frac{1}{y}}{y-z}</code></td>
    </tr>
</table>

**Непрерывные дроби**

Непрерывные дроби следует записывать с помощью команды `\cfrac`.

```latex
\begin{equation}
    x = a_0 
        + \cfrac{1}{a_1 
        + \cfrac{1}{a_2 
        + \cfrac{1}{a_3 
        + \cfrac{1}{a_4} 
    } } }
\end{equation}
```

$$
\begin{equation}
    x = a_0 
        + \cfrac{1}{a_1 
        + \cfrac{1}{a_2 
        + \cfrac{1}{a_3 
        + \cfrac{1}{a_4} 
    } } }
\end{equation}
$$

**Умножение двух чисел**

Чтобы сделать умножение визуально похожим на дробь, можно использовать вложенный массив, например, умножение чисел, написанных одно под другим.

```latex
\begin{equation}
    \frac{
        \begin{array}[b]{r}
            \left( x_1 x_2 \right) \\
            \times \left( x'_1 x'_2 \right)
        \end{array}
    }
    {
        \left( y_1y_2y_3y_4 \right)
    }
\end{equation}
```

$$
\begin{equation}
    \frac{
        \begin{array}[b]{r}
            \left( x_1 x_2 \right) \\
            \times \left( x'_1 x'_2 \right)
        \end{array}
    }
    {
        \left( y_1y_2y_3y_4 \right)
    }
\end{equation}
$$

<!-- Roots -->
<h5 id="roots">Корни (Roots) <a href="#top">↑top↑</a></h5>

Команда `\sqrt` создаёт символ квадратного корня, окружающий математическое выражение. Он принимает необязательный аргумент в квадратных скобках 
(`[` и `]`) для изменения показателя (степени) корня:

<table>
    <tr>
        <td>$\sqrt{\frac{a}{b}}$</td>
        <td><code>\sqrt{\frac{a}{b}}</code></td>
    </tr>
</table>

<table>
    <tr>
        <td>$\sqrt[n]{1+x+x^2+x^3+\dots+x^n}$</td>
        <td><code>\sqrt[n]{1+x+x^2+x^3+\dots+x^n}</code></td>
    </tr>
</table>

<!-- Parentheses and Separators -->
<h5 id="parentheses-separators">Скобки и разделители (Parentheses and Separators) <a href="#top">↑top↑</a></h5>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$( a )$</td>
        <td><code>( a )</code></td>
    </tr>
    <tr>
        <td>$[ b ]$</td>
        <td><code>[ b ]</code><br><code>\lbrack b \rbrack</code></td>
    </tr>
    <tr>
        <td>$\{ c \}$</td>
        <td><code>\{ c \}</code></td>
    </tr>
    <tr>
        <td>$| d |$</td>
        <td><code>| d |</code></td>
    </tr>
    <tr>
        <td>$\| e \|$</td>
        <td><code>\| e \|</code></td>
    </tr>
    <tr>
        <td>$\langle f \rangle$</td>
        <td><code>\langle f \rangle</code></td>
    </tr>
    <tr>
        <td>$\lfloor g \rfloor$</td>
        <td><code>\lfloor g \rfloor</code></td>
    </tr>
    <tr>
        <td>$\lceil h \rceil$</td>
        <td><code>\lceil h \rceil</code></td>
    </tr>
    <tr>
        <td>$\ulcorner i \urcorner$</td>
        <td><code>\ulcorner i \urcorner</code></td>
    </tr>
    <tr>
        <td>$/ j \backslash$</td>
        <td><code>/ j \backslash</code></td>
    </tr>
</table>

**Автоматическое определение размеров**

Очень часто математические функции будут отличаться друг от друга по размеру, и в этом случае разделители, окружающие выражение, должны изменяться 
соответственно. Это можно сделать автоматически с помощью команд `\left`, `\right`, и `\middle`. Любой из выше перечисленных разделителей может быть 
использован в сочетании с этими командами.

<table>
    <tr>
        <td>$\left(\frac{x^2}{y^3}\right)$</td>
        <td><code>\left(\frac{x^2}{y^3}\right)</code></td>
    </tr>
</table>

<table>
    <tr>
        <td>$P\left(A=2\middle|\frac{A^2}{B}>4\right)$</td>
        <td><code>P\left(A=2\middle|\frac{A^2}{B}>4\right)</code></td>
    </tr>
</table>

Фигурные скобки определяются иначе, с помощью `\left\{` и `\right\}`

<table>
    <tr>
        <td>$\left\{\frac{x^2}{y^3}\right\}$</td>
        <td><code>\left\{\frac{x^2}{y^3}\right\}</code></td>
    </tr>
</table>

Если разделитель нужен только с одной стороны выражения, то с другой стороны разделить может быть обозначен точкой (`.`), что сделает его невидимым.

<table>
    <tr>
        <td>$\left.\frac{x^3}{3}\right|_0^1$</td>
        <td><code>\left.\frac{x^3}{3}\right|_0^1</code></td>
    </tr>
</table>

**Ручное определение размеров**

В некоторых случаях автоматический размер, создаваемый командами `\left` и `\right`, может быть отличен от того, что вы ожидаете увидеть, или вам 
требуется более точно контролировать размеры разделителей. В этом случае могут использоваться команды-модификаторы `\big`, `\Big`, `\bigg` и `\Bigg`:

<table>
    <tr>
        <td>$( \big( \Big( \bigg( \Bigg( \Bigg) \bigg) \Big) \big) )$</td>
        <td><code>\left.\frac{x^3}{3}\right|_0^1</code></td>
    </tr>
</table>

<!-- Limits -->
<h5 id="limits">Пределы (Limits) <a href="#top">↑top↑</a></h5>

Для рядов и интегралов можно указать приделы в корректном формате (без степеней и индексов) с помоштю команды `\limits`, где значения будут указаны 
выше или ниже символа.

<table>
    <tr>
        <td>$\int\limits_a^b$</td>
        <td><code>\int\limits_a^b</code></td>
    </tr>
</table>

<table>
    <tr>
        <td>$\sum\limits_{i=1}^\infty$</td>
        <td><code>\sum\limits_{i=1}^\infty</code></td>
    </tr>
</table>

---

<!-- Series and Integrals -->
<h4 id="series-integrals">Ряды и интегралы (Series and Integrals) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$\sum$</td>
        <td><code>\sum</code></td>
    </tr>
    <tr>
        <td>$\prod$</td>
        <td><code>\prod</code></td>
    </tr>
    <tr>
        <td>$\coprod$</td>
        <td><code>\coprod</code></td>
    </tr>
    <tr>
        <td>$\bigoplus$</td>
        <td><code>\bigoplus</code></td>
    </tr>
    <tr>
        <td>$\bigotimes$</td>
        <td><code>\bigotimes</code></td>
    </tr>
    <tr>
        <td>$\bigodot$</td>
        <td><code>\bigodot</code></td>
    </tr>
    <tr>
        <td>$\bigcup$</td>
        <td><code>\bigcup</code></td>
    </tr>
    <tr>
        <td>$\bigcap$</td>
        <td><code>\bigcap</code></td>
    </tr>
    <tr>
        <td>$\biguplus$</td>
        <td><code>\biguplus</code></td>
    </tr>
    <tr>
        <td>$\bigsqcup$</td>
        <td><code>\bigsqcup</code></td>
    </tr>
    <tr>
        <td>$\bigvee$</td>
        <td><code>\bigvee</code></td>
    </tr>
    <tr>
        <td>$\bigwedge$</td>
        <td><code>\bigwedge</code></td>
    </tr>
    <tr>
        <td>$\int$</td>
        <td><code>\int</code></td>
    </tr>
    <tr>
        <td>$\oint$</td>
        <td><code>\oint</code></td>
    </tr>
    <tr>
        <td>$\iint$</td>
        <td><code>\iint</code></td>
    </tr>
    <tr>
        <td>$\iiint$</td>
        <td><code>\iiint</code></td>
    </tr>
    <tr>
        <td>$\iiiint$</td>
        <td><code>\iiiint</code></td>
    </tr>
    <tr>
        <td>$\idotsint$</td>
        <td><code>\idotsint</code></td>
    </tr>
</table>

---

<!-- Relation Symbols -->
<h4 id="relation-symbols">Символы отношений (Relation Symbols) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$<$</td>
        <td><code><</code></td>
    </tr>
    <tr>
        <td>$>$</td>
        <td><code>></code></td>
    </tr>
    <tr>
        <td>$=$</td>
        <td><code>=</code></td>
    </tr>
    <tr>
        <td>$\parallel$</td>
        <td><code>\parallel</code></td>
    </tr>
    <tr>
        <td>$\nparallel$</td>
        <td><code>\nparallel</code></td>
    </tr>
    <tr>
        <td>$\leq$</td>
        <td><code>\leq</code></td>
    </tr>
    <tr>
        <td>$\geq$</td>
        <td><code>\geq</code></td>
    </tr>
    <tr>
        <td>$\doteq$</td>
        <td><code>\doteq</code></td>
    </tr>
    <tr>
        <td>$\asymp$</td>
        <td><code>\asymp</code></td>
    </tr>
    <tr>
        <td>$\bowtie$</td>
        <td><code>\bowtie</code></td>
    </tr>
    <tr>
        <td>$\ll$</td>
        <td><code>\ll</code></td>
    </tr>
    <tr>
        <td>$\gg$</td>
        <td><code>\gg</code></td>
    </tr>
    <tr>
        <td>$\equiv$</td>
        <td><code>\equiv</code></td>
    </tr>
    <tr>
        <td>$\vdash$</td>
        <td><code>\vdash</code></td>
    </tr>
    <tr>
        <td>$\dashv$</td>
        <td><code>\dashv</code></td>
    </tr>
    <tr>
        <td>$\subset$</td>
        <td><code>\subset</code></td>
    </tr>
    <tr>
        <td>$\supset$</td>
        <td><code>\supset</code></td>
    </tr>
    <tr>
        <td>$\approx$</td>
        <td><code>\approx</code></td>
    </tr>
    <tr>
        <td>$\in$</td>
        <td><code>\in</code></td>
    </tr>
    <tr>
        <td>$\ni$</td>
        <td><code>\ni</code></td>
    </tr>
    <tr>
        <td>$\subseteq$</td>
        <td><code>\subseteq</code></td>
    </tr>
    <tr>
        <td>$\supseteq$</td>
        <td><code>\supseteq</code></td>
    </tr>
    <tr>
        <td>$\cong$</td>
        <td><code>\cong</code></td>
    </tr>
    <tr>
        <td>$\smile$</td>
        <td><code>\smile</code></td>
    </tr>
    <tr>
        <td>$\frown$</td>
        <td><code>\frown</code></td>
    </tr>
    <tr>
        <td>$\nsubseteq$</td>
        <td><code>\nsubseteq</code></td>
    </tr>
    <tr>
        <td>$\nsupseteq$</td>
        <td><code>\nsupseteq</code></td>
    </tr>
    <tr>
        <td>$\simeq$</td>
        <td><code>\simeq</code></td>
    </tr>
    <tr>
        <td>$\models$</td>
        <td><code>\models</code></td>
    </tr>
    <tr>
        <td>$\notin$</td>
        <td><code>\notin</code></td>
    </tr>
    <tr>
        <td>$\sqsupset$</td>
        <td><code>\sqsupset</code></td>
    </tr>
    <tr>
        <td>$\sim$</td>
        <td><code>\sim</code></td>
    </tr>
    <tr>
        <td>$\perp$</td>
        <td><code>\perp</code></td>
    </tr>
    <tr>
        <td>$\mid$</td>
        <td><code>\mid</code></td>
    </tr>
    <tr>
        <td>$\sqsubseteq$</td>
        <td><code>\sqsubseteq</code></td>
    </tr>
    <tr>
        <td>$\sqsupseteq$</td>
        <td><code>\sqsupseteq</code></td>
    </tr>
    <tr>
        <td>$\propto$</td>
        <td><code>\propto</code></td>
    </tr>
    <tr>
        <td>$\prec$</td>
        <td><code>\prec</code></td>
    </tr>
    <tr>
        <td>$\succ$</td>
        <td><code>\succ</code></td>
    </tr>
    <tr>
        <td>$\preceq$</td>
        <td><code>\preceq</code></td>
    </tr>
    <tr>
        <td>$\succeq$</td>
        <td><code>\succeq</code></td>
    </tr>
    <tr>
        <td>$\neq$</td>
        <td><code>\neq</code></td>
    </tr>
    <tr>
        <td>$\sphericalangle$</td>
        <td><code>\sphericalangle</code></td>
    </tr>
    <tr>
        <td>$\measuredangle$</td>
        <td><code>\measuredangle</code></td>
    </tr>
    <tr>
        <td>$\therefore$</td>
        <td><code>\therefore</code></td>
    </tr>
    <tr>
        <td>$\because$</td>
        <td><code>\because</code></td>
    </tr>
</table>

---

<!-- Binary Operations -->
<h4 id="binary-operations">Бинарные операции (Binary Operations) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$\pm$</td>
        <td><code>\pm</code></td>
    </tr>
    <tr>
        <td>$\mp$</td>
        <td><code>\mp</code></td>
    </tr>
    <tr>
        <td>$\times$</td>
        <td><code>\times</code></td>
    </tr>
    <tr>
        <td>$\div$</td>
        <td><code>\div</code></td>
    </tr>
    <tr>
        <td>$\ast$</td>
        <td><code>\ast</code></td>
    </tr>
    <tr>
        <td>$\star$</td>
        <td><code>\star</code></td>
    </tr>
    <tr>
        <td>$\dagger$</td>
        <td><code>\dagger</code></td>
    </tr>
    <tr>
        <td>$\ddagger$</td>
        <td><code>\ddagger</code></td>
    </tr>
    <tr>
        <td>$\cap$</td>
        <td><code>\cap</code></td>
    </tr>
    <tr>
        <td>$\cup$</td>
        <td><code>\cup</code></td>
    </tr>
    <tr>
        <td>$\uplus$</td>
        <td><code>\uplus</code></td>
    </tr>
    <tr>
        <td>$\sqcap$</td>
        <td><code>\sqcap</code></td>
    </tr>
    <tr>
        <td>$\sqcup$</td>
        <td><code>\sqcup</code></td>
    </tr>
    <tr>
        <td>$\vee$</td>
        <td><code>\vee</code></td>
    </tr>
    <tr>
        <td>$\wedge$</td>
        <td><code>\wedge</code></td>
    </tr>
    <tr>
        <td>$\cdot$</td>
        <td><code>\cdot</code></td>
    </tr>
    <tr>
        <td>$\diamond$</td>
        <td><code>\diamond</code></td>
    </tr>
    <tr>
        <td>$\bigtriangleup$</td>
        <td><code>\bigtriangleup</code></td>
    </tr>
    <tr>
        <td>$\bigtriangledown$</td>
        <td><code>\bigtriangledown</code></td>
    </tr>
    <tr>
        <td>$\triangleleft$</td>
        <td><code>\triangleleft</code></td>
    </tr>
    <tr>
        <td>$\triangleright$</td>
        <td><code>\triangleright</code></td>
    </tr>
    <tr>
        <td>$\bigcirc$</td>
        <td><code>\bigcirc</code></td>
    </tr>
    <tr>
        <td>$\bullet$</td>
        <td><code>\bullet</code></td>
    </tr>
    <tr>
        <td>$\wr$</td>
        <td><code>\wr</code></td>
    </tr>
    <tr>
        <td>$\oplus$</td>
        <td><code>\oplus</code></td>
    </tr>
    <tr>
        <td>$\ominus$</td>
        <td><code>\ominus</code></td>
    </tr>
    <tr>
        <td>$\otimes$</td>
        <td><code>\otimes</code></td>
    </tr>
    <tr>
        <td>$\oslash$</td>
        <td><code>\oslash</code></td>
    </tr>
    <tr>
        <td>$\odot$</td>
        <td><code>\odot</code></td>
    </tr>
    <tr>
        <td>$\circ$</td>
        <td><code>\circ</code></td>
    </tr>
    <tr>
        <td>$\setminus$</td>
        <td><code>\setminus</code></td>
    </tr>
    <tr>
        <td>$\amalg$</td>
        <td><code>\amalg</code></td>
    </tr>
</table>

---

<!-- Set and/or Logic Notation -->
<h4 id="logic-notation">Обозначение набора и/или логики (Set and/or Logic Notation) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$\exists$</td>
        <td><code>\exists</code></td>
    </tr>
    <tr>
        <td>$\nexists$</td>
        <td><code>\nexists</code></td>
    </tr>
    <tr>
        <td>$\forall$</td>
        <td><code>\forall</code></td>
    </tr>
    <tr>
        <td>$\neg$</td>
        <td><code>\neg</code></td>
    </tr>
    <tr>
        <td>$\subset$</td>
        <td><code>\subset</code></td>
    </tr>
     <tr>
        <td>$\supset$</td>
        <td><code>\supset</code></td>
    </tr>
    <tr>
        <td>$\in$</td>
        <td><code>\in</code></td>
    </tr>
    <tr>
        <td>$\notin$</td>
        <td><code>\notin</code></td>
    </tr>
    <tr>
        <td>$\ni$</td>
        <td><code>\ni</code></td>
    </tr>
    <tr>
        <td>$\land$</td>
        <td><code>\land</code></td>
    </tr>
     <tr>
        <td>$\lor$</td>
        <td><code>\lor</code></td>
    </tr>
    <tr>
        <td>$\angle$</td>
        <td><code>\angle</code></td>
    </tr>
    <tr>
        <td>$\rightarrow$</td>
        <td><code>\rightarrow</code><br><code>\to</code></td>
    </tr>
    <tr>
        <td>$\leftarrow$</td>
        <td><code>\leftarrow</code><br><code>\gets</code></td>
    </tr>
    <tr>
        <td>$\mapsto$</td>
        <td><code>\mapsto</code></td>
    </tr>
     <tr>
        <td>$\implies$</td>
        <td><code>\implies</code></td>
    </tr>
    <tr>
        <td>$\impliedby$</td>
        <td><code>\impliedby</code></td>
    </tr>
    <tr>
        <td>$\Rightarrow$</td>
        <td><code>\Rightarrow</code><br><code>\implies</code></td>
    </tr>
    <tr>
        <td>$\leftrightarrow$</td>
        <td><code>\leftrightarrow</code></td>
    </tr>
     <tr>
        <td>$\Leftrightarrow$</td>
        <td><code>\Leftrightarrow</code></td>
    </tr>
    <tr>
        <td>$\top$</td>
        <td><code>\top</code></td>
    </tr>
    <tr>
        <td>$\bot$</td>
        <td><code>\bot</code></td>
    </tr>
    <tr>
        <td>$\emptyset$</td>
        <td><code>\emptyset</code></td>
    </tr>
    <tr>
        <td>$\varnothing$</td>
        <td><code>\varnothing</code></td>
    </tr>
    <tr>
        <td>$\rightleftharpoons$</td>
        <td><code>\rightleftharpoons</code></td>
    </tr>
</table>

---

<!-- Delimiters -->
<h4 id="delimiters">Разделители (Delimiters) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$|$</td>
        <td><code>|</code><br><code>\mid</code></td>
    </tr>
    <tr>
        <td>$\|$</td>
        <td><code>\|</code></td>
    </tr>
    <tr>
        <td>$/$</td>
        <td><code>/</code></td>
    </tr>
    <tr>
        <td>$\backslash$</td>
        <td><code>\backslash</code></td>
    </tr>
    <tr>
        <td>$\{$</td>
        <td><code>\{</code></td>
    </tr>
    <tr>
        <td>$\}$</td>
        <td><code>\}</code></td>
    </tr>
    <tr>
        <td>$\langle$</td>
        <td><code>\langle</code></td>
    </tr>
    <tr>
        <td>$\rangle$</td>
        <td><code>\rangle</code></td>
    </tr>
    <tr>
        <td>$\uparrow$</td>
        <td><code>\uparrow</code></td>
    </tr>
    <tr>
        <td>$\Uparrow$</td>
        <td><code>\Uparrow</code></td>
    </tr>
    <tr>
        <td>$\lceil$</td>
        <td><code>\lceil</code></td>
    </tr>
    <tr>
        <td>$\rceil$</td>
        <td><code>\rceil</code></td>
    </tr>
    <tr>
        <td>$\downarrow$</td>
        <td><code>\downarrow</code></td>
    </tr>
    <tr>
        <td>$\Downarrow$</td>
        <td><code>\Downarrow</code></td>
    </tr>
    <tr>
        <td>$\lfloor$</td>
        <td><code>\lfloor</code></td>
    </tr>
    <tr>
        <td>$\rfloor$</td>
        <td><code>\rfloor</code></td>
    </tr>
</table>

---

<!-- Greek Letters -->
<h4 id="greek-letters">Греческие буквы (Greek Letters) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$A$ and $alpha$</td>
        <td><code>A</code> and <code>alpha</code></td>
    </tr>
    <tr>
        <td>$B$ and $\beta$</td>
        <td><code>B</code> and <code>\beta</code></td>
    </tr>
    <tr>
        <td>$\Gamma$ and $\gamma$</td>
        <td><code>\Gamma</code> and <code>\gamma</code></td>
    </tr>
    <tr>
        <td>$\Delta$ and $\delta$</td>
        <td><code>\Delta</code> and <code>\delta</code></td>
    </tr>
    <tr>
        <td>$E$, $\epsilon$ and $\varepsilon$</td>
        <td><code>E</code>, <code>\epsilon</code> and <code>\varepsilon</code></td>
    </tr>
    <tr>
        <td>$Z$ and $\zeta$</td>
        <td><code>Z</code> and <code>\zeta</code></td>
    </tr>
    <tr>
        <td>$H$ and $\eta$</td>
        <td><code>H</code> and <code>\eta</code></td>
    </tr>
    <tr>
        <td>$\Theta$, $\theta$ and $\vartheta$</td>
        <td><code>\Theta</code>, <code>\theta</code> and <code>\vartheta</code></td>
    </tr>
    <tr>
        <td>$I$ and $\iota$</td>
        <td><code>I</code> and <code>\iota</code></td>
    </tr>
    <tr>
        <td>$K$, $\kappa$ and $\varkappa$</td>
        <td><code>K</code>, <code>\kappa</code> and <code>\varkappa</code></td>
    </tr>
    <tr>
        <td>$\Lambda$ and $\lambda$</td>
        <td><code>\Lambda</code> and <code>\lambda</code></td>
    </tr>
    <tr>
        <td>$M$ and $\mu$</td>
        <td><code>M</code> and <code>\mu</code></td>
    </tr>
    <tr>
        <td>$N$ and $\nu$</td>
        <td><code>N</code> and <code>\nu</code></td>
    </tr>
    <tr>
        <td>$\Xi$ and $\xi$</td>
        <td><code>\Xi</code> and <code>\xi</code></td>
    </tr>
    <tr>
        <td>$O$ and $o$</td>
        <td><code>O</code> and <code>o</code></td>
    </tr>
    <tr>
        <td>$\Pi$, $\pi$ and $\varpi$</td>
        <td><code>\Pi</code>, <code>\pi</code> and <code>\varpi</code></td>
    </tr>
    <tr>
        <td>$P$, $\rho$ and $\varrho$</td>
        <td><code>P</code>, <code>\rho</code> and <code>\varrho</code></td>
    </tr>
    <tr>
        <td>$\Sigma$, $\sigma$ and $\varsigma$</td>
        <td><code>\Sigma</code>, <code>\sigma</code> and <code>\varsigma</code></td>
    </tr>
    <tr>
        <td>$T$ and $\tau$</td>
        <td><code>T</code> and <code>\tau</code></td>
    </tr>
    <tr>
        <td>$\Upsilon$ and $\upsilon$</td>
        <td><code>\Upsilon</code> and <code>\upsilon</code></td>
    </tr>
    <tr>
        <td>$\Phi$, $\phi$ and $\varphi$</td>
        <td><code>\Phi</code>, <code>\phi</code> and <code>\varphi</code></td>
    </tr>
    <tr>
        <td>$X$ and $\chi$</td>
        <td><code>X</code> and <code>\chi</code></td>
    </tr>
    <tr>
        <td>$\Psi$ and $\psi$</td>
        <td><code>\Psi</code> and <code>\psi</code></td>
    </tr>
    <tr>
        <td>$\Omega$ and $\omega$</td>
        <td><code>\Omega</code> and <code>\omega</code></td>
    </tr>
</table>

---

<!-- Other Symbols -->
<h4 id="other-symbols">Другие символы (Other Symbols) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$\partial$</td>
        <td><code>\partial</code></td>
    </tr>
    <tr>
        <td>$\eth$</td>
        <td><code>\eth</code></td>
    </tr>
    <tr>
        <td>$\hbar$</td>
        <td><code>\hbar</code></td>
    </tr>
    <tr>
        <td>$\imath$</td>
        <td><code>\imath</code></td>
    </tr>
    <tr>
        <td>$\jmath$</td>
        <td><code>\jmath</code></td>
    </tr>
    <tr>
        <td>$\ell$</td>
        <td><code>\ell</code></td>
    </tr>
    <tr>
        <td>$\Re$</td>
        <td><code>\Re</code></td>
    </tr>
    <tr>
        <td>$\Im$</td>
        <td><code>\Im</code></td>
    </tr>
    <tr>
        <td>$\wp$</td>
        <td><code>\wp</code></td>
    </tr>
    <tr>
        <td>$\nabla$</td>
        <td><code>\nabla</code></td>
    </tr>
    <tr>
        <td>$\Box$</td>
        <td><code>\Box</code></td>
    </tr>
    <tr>
        <td>$\infty$</td>
        <td><code>\infty</code></td>
    </tr>
    <tr>
        <td>$\aleph$</td>
        <td><code>\aleph</code></td>
    </tr>
    <tr>
        <td>$\beth$</td>
        <td><code>\beth</code></td>
    </tr>
    <tr>
        <td>$\gimel$</td>
        <td><code>\gimel</code></td>
    </tr>
</table>

---

<!-- Trigonometric Functions -->
<h4 id="trigonometric-functions">Тригонометрические функции (Trigonometric Functions) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$\sin$</td>
        <td><code>\sin</code></td>
    </tr>
    <tr>
        <td>$\cos$</td>
        <td><code>\cos</code></td>
    </tr>
    <tr>
        <td>$\tan$</td>
        <td><code>\tan</code></td>
    </tr>
    <tr>
        <td>$\cot$</td>
        <td><code>\cot</code></td>
    </tr>
    <tr>
        <td>$\arcsin$</td>
        <td><code>\arcsin</code></td>
    </tr>
    <tr>
        <td>$\arccos$</td>
        <td><code>\arccos</code></td>
    </tr>
    <tr>
        <td>$\arctan$</td>
        <td><code>\arctan</code></td>
    </tr>
    <tr>
        <td>$\sinh$</td>
        <td><code>\sinh</code></td>
    </tr>
    <tr>
        <td>$\cosh$</td>
        <td><code>\cosh</code></td>
    </tr>
    <tr>
        <td>$\tanh$</td>
        <td><code>\tanh</code></td>
    </tr>
    <tr>
        <td>$\coth$</td>
        <td><code>\coth</code></td>
    </tr>
    <tr>
        <td>$\sec$</td>
        <td><code>\sec</code></td>
    </tr>
    <tr>
        <td>$\csc$</td>
        <td><code>\csc</code></td>
    </tr>
</table>

---

<!-- Dots -->
<h4 id="dots">Точки (Dots) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$\dots$</td>
        <td><code>\dots</code></td>
    </tr>
    <tr>
        <td>$\ldots$</td>
        <td><code>\ldots</code></td>
    </tr>
    <tr>
        <td>$\cdots$</td>
        <td><code>\cdots</code></td>
    </tr>
    <tr>
        <td>$\vdots$</td>
        <td><code>\vdots</code></td>
    </tr>
    <tr>
        <td>$\ddots$</td>
        <td><code>\ddots</code></td>
    </tr>
</table>

<!-- Accents -->
<h4 id="accents">Акценты (Accents) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$a'$</td>
        <td><code>a'</code><br><code>a^{\prime}</code></td>
    </tr>
    <tr>
        <td>$a''$</td>
        <td><code>a''</code></td>
    </tr>
    <tr>
        <td>$\hat{a}$</td>
        <td><code>\hat{a}</code></td>
    </tr>
    <tr>
        <td>$\bar{a}$</td>
        <td><code>\bar{a}</code></td>
    </tr>
    <tr>
        <td>$\grave{a}$</td>
        <td><code>\grave{a}</code></td>
    </tr>
    <tr>
        <td>$\acute{a}$</td>
        <td><code>\acute{a}</code></td>
    </tr>
    <tr>
        <td>$\dot{a}$</td>
        <td><code>\dot{a}</code></td>
    </tr>
    <tr>
        <td>$\ddot{a}$</td>
        <td><code>\ddot{a}</code></td>
    </tr>
    <tr>
        <td>$\not{a}$</td>
        <td><code>\not{a}</code></td>
    </tr>
    <tr>
        <td>$\mathring{a}$</td>
        <td><code>\mathring{a}</code></td>
    </tr>
    <tr>
        <td>$\overrightarrow{AB}$</td>
        <td><code>\overrightarrow{AB}</code></td>
    </tr>
    <tr>
        <td>$\overleftarrow{AB}$</td>
        <td><code>\overleftarrow{AB}</code></td>
    </tr>
    <tr>
        <td>$a'''$</td>
        <td><code>a'''</code></td>
    </tr>
    <tr>
        <td>$a''''$</td>
        <td><code>a''''</code></td>
    </tr>
    <tr>
        <td>$\overline{aaa}$</td>
        <td><code>\overline{aaa}</code></td>
    </tr>
    <tr>
        <td>$\check{a}$</td>
        <td><code>\check{a}</code></td>
    </tr>
    <tr>
        <td>$\breve{a}$</td>
        <td><code>\breve{a}</code></td>
    </tr>
    <tr>
        <td>$\vec{a}$</td>
        <td><code>\vec{a}</code></td>
    </tr>
    <tr>
        <td>$\dddot{a}$</td>
        <td><code>\dddot{a}</code></td>
    </tr>
    <tr>
        <td>$\ddddot{a}$</td>
        <td><code>\ddddot{a}</code></td>
    </tr>
    <tr>
        <td>$\widehat{AAA}$</td>
        <td><code>\widehat{AAA}</code></td>
    </tr>
    <tr>
        <td>$\widetilde{AAA}$</td>
        <td><code>\widetilde{AAA}</code></td>
    </tr>
    <tr>
        <td>$\stackrel\frown{AAA}$</td>
        <td><code>\stackrel\frown{AAA}</code></td>
    </tr>
    <tr>
        <td>$\tilde{a}$</td>
        <td><code>\tilde{a}</code></td>
    </tr>
    <tr>
        <td>$\underline{a}$</td>
        <td><code>\underline{a}</code></td>
    </tr>
</table>

<!-- Fonts -->
<h4 id="fonts">Шрифты (Fonts) <a href="#top">↑top↑</a></h4>

<table>
    <tr>
        <th>Symbol</th>
        <th>Script</th>
    </tr>
    <tr>
        <td>$\mathnormal{ABCDEF}$ $\mathnormal{abcdef}$ $\mathnormal{123456}$</td>
        <td><code>\mathnormal{ABCDEF} \mathnormal{abcdef} \mathnormal{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathrm{ABCDEF}$ $\mathrm{abcdef}$ $\mathrm{123456}$</td>
        <td><code>\mathrm{ABCDEF} \mathrm{abcdef} \mathrm{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathit{ABCDEF}$ $\mathit{abcdef}$ $\mathit{123456}$</td>
        <td><code>\mathit{ABCDEF} \mathit{abcdef} \mathit{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathbf{ABCDEF}$ $\mathbf{abcdef}$ $\mathbf{123456}$</td>
        <td><code>\mathbf{ABCDEF} \mathbf{abcdef} \mathbf{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathsf{ABCDEF}$ $\mathsf{abcdef}$ $\mathsf{123456}$</td>
        <td><code>\mathsf{ABCDEF} \mathsf{abcdef} \mathsf{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathtt{ABCDEF}$ $\mathtt{abcdef}$ $\mathtt{123456}$</td>
        <td><code>\mathtt{ABCDEF} \mathtt{abcdef} \mathtt{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathfrak{ABCDEF}$ $\mathfrak{abcdef}$ $\mathfrak{123456}$</td>
        <td><code>\mathfrak{ABCDEF} \mathfrak{abcdef} \mathfrak{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathcal{ABCDEF}$ $\mathcal{abcdef}$ $\mathcal{123456}$</td>
        <td><code>\mathcal{ABCDEF} \mathcal{abcdef} \mathcal{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathbb{ABCDEF}$ $\mathbb{abcdef}$ $\mathbb{123456}$</td>
        <td><code>\mathbb{ABCDEF} \mathbb{abcdef} \mathbb{123456}</code></td>
    </tr>
    <tr>
        <td>$\mathscr{ABCDEF}$ $\mathscr{abcdef}$ $\mathscr{123456}$</td>
        <td><code>\mathscr{ABCDEF} \mathscr{abcdef} \mathscr{123456}</code></td>
    </tr>
</table>

---

<!-- Matrices and arrays -->
<h4 id="matrices-arrays">Матрицы и массивы (Matrices and Arrays) <a href="#top">↑top↑</a></h4>

В базовой матрице, как и в других табличных структурах, записи указываются по строкам, столбцы разделяются амперсандом (`&`), а новые строки 
разделяются двойной обратной косой чертой (`\\`).

```latex
\begin{matrix}
a & b & c \\
d & e & f \\
g & h & i
\end{matrix}
```

$$
\begin{matrix}
a & b & c \\
d & e & f \\
g & h & i
\end{matrix}
$$

При записи матриц произвольного размера обычно используются горизонтальные, вертикальные и диагональные тройки точек для заполнения 
определенных столбцов и строк. Их можно указать с помощью `\cdots`, `\vdots` и `\ddots` соответственно.

```latex
A_{m,n} = 
\begin{pmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
\vdots  & \vdots  & \ddots & \vdots  \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n} 
\end{pmatrix}
```

$$
A_{m,n} = 
\begin{pmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
\vdots  & \vdots  & \ddots & \vdots  \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n} 
\end{pmatrix}
$$

В некоторых случаях вам может потребоваться более точный контроль выравнивания внутри каждого столбца или вставка строк между столбцами или строками.

```latex
\begin{array}{c|c}
1 & 2 \\ 
\hline
3 & 4
\end{array}
```

$$
\begin{array}{c|c}
1 & 2 \\ 
\hline
3 & 4
\end{array}
$$

```latex
M = 
\begin{bmatrix}
\frac{5}{6} & \frac{1}{6} & 0           \\
\frac{5}{6} & 0           & \frac{1}{6} \\
0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
```

$$
M = 
\begin{bmatrix}
\frac{5}{6} & \frac{1}{6} & 0           \\
\frac{5}{6} & 0           & \frac{1}{6} \\
0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$

---

<!-- Contacts -->
<h2>📡 Контакты автора:</h2>
<div id="badges" align="center">
    <a href="https://vk.com/bogdan_klimov">
        <img src="https://img.shields.io/badge/VK-blue?style=for-the-badge&logo=vk&logoColor=white&size=30" alt="VK Badge"/>
    </a> &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://t.me/bogdanklimov">
        <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram Badge"/>
    </a> &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://www.instagram.com/ghost_777_24?igsh=aHdwa2s1cTIzbmhw&utm_source=qr">
        <img src="https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white" alt="Instagram Badge"/>
    </a> &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://www.facebook.com/profile.php?id=100033935590093&mibextid=LQQJ4d">
        <img src="https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white" alt="Facebook Badge"/>
    </a>
</div>
