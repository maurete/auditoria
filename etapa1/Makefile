# nombre de los archivos fuente
fuente = main.tex
dep = conf/comandos.tex conf/config.tex conf/fuentes.tex \
conf/packages.tex conf/preconfig.tex
aux = $(fuente:%.tex=%.aux) $(fuente:%.tex=%.log) $(fuente:%.tex=%.out) \
$(dep:%.tex=%.aux)
pdfs = cv.pdf img/01.pdf img/02.pdf img/03.pdf img/04.pdf img/05.pdf \
img/06.pdf img/07.pdf img/08.pdf letter.pdf
# 'compilador':
cc = pdflatex -interaction nonstopmode
latex = latex

all : pdflatex

pdflatex : $(fuente) $(dep)
	$(cc) $(fuente)
	$(cc) $(fuente)
	rm -f $(aux) 

latex : $(fuente) $(dep)
	$(latex) $(fuente)
	$(latex) $(fuente)
	dvipdf $(fuente:%.tex=%.dvi)
	rm -f $(fuente:%.tex=%.dvi) $(aux)

clean:
	rm -f $(fuente:%.tex=%.pdf) $(fuente:%.tex=%.dvi)