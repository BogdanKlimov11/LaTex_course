Используя пакет listings в LaTeX мы можем добавлять код написанный на разных языках программирования. 
Он умеет подсвечивать код, считать строки и многое другое…

Чтобы использовать listing пакет, Вы должны его подключить:

```latex
usepackage{listings}
```

Для того чтобы вставить программный код, мы должны использовать следующую конструкцию:

```latex
begin{lstlisting}
put your code here
end{lstlisting}
```

Другой способ вставить код, очень полезен, если Вы еще занимаетесь его редактированием. Таким образом, 
если вы изменяете исходный код, вы просто должны перекомпилировать код LaTeX и ваш документ будет 
обновлен. Для этого используйте следующий код:

```latex
lstinputlisting{source_filename.py}
```

В примере мы используем Python файл, но Вы можете добавлять любой файл содержащий программный код.
Если код не подсвечивается, значит компилятор не смог определить язык на котором написан код. Мы можем 
определить язык вручную следующей командой:

```latex
lstinputlisting[language=Python]{source_filename.py}
```

Пакет listing поддерживает следующие языки программирования:
* ABAP
* IDL
* PL/I
* ACSL
* inform
* Plasm
* Ada
* Java
* POV
* Algol
* JVMIS
* Prolog
* Ant
* ksh
* Promela
* Assembler2
* Lisp
* Python
* Awk
* Logo
* R
* bash
* make
* Reduce
* Basic2
* Mathematica1
* Rexx
* C
* Matlab
* RSL
* C++
* Mercury
* Ruby
* Caml
* MetaPost
* S
* Clean
* Miranda
* SAS
* Cobol
* Mizar
* Scilab
* Comal
* ML
* sh
* csh
* Modelica3
* SHELXL
* Delphi
* Modula-2
* Simula
* Eiffel
* MuPAD
* SQL
* Elan
* NASTRAN
* tcl
* erlang
* Oberon-2
* TeX
* Euphoria
* OCL
* VBScript
* Fortran
* Octave
* Verilog
* GCL
* Oz
* VHDL
* Gnuplot
* Pascal
* VRML
* Haskell
* Perl
* XML
* HTML
* PHP
* XSLT

Также поддерживаются другие диалекты. Полный список Вы можете найти в <a href="http://mirror.hmc.edu/ctan/macros/latex/contrib/listings/listings.pdf">документации</a>.

Пример конфигурации пакета listing Вы можете найти <a href="https://github.com/BogdanKlimov11/LaTex_course/blob/main/Listing_code_in_LaTeX/Listing_package_configurations.tex">здесь</a>.
