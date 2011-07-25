# nombre de los archivos fuente
fuentes = main.tex presentacion.tex
texes = $(wildcard '*.tex')
dep = conf/comandos.tex conf/config.tex conf/fuentes.tex \
conf/packages.tex conf/preconfig.tex
fuentes_aux = $(fuentes:%.tex=%.aux) $(fuentes:%.tex=%.log) $(fuentes:%.tex=%.out) \
$(dep:%.tex=%.aux)

# 'compilador':
cc = pdflatex -interaction nonstopmode
latex = latex

all:	$(fuentes:%.tex=%.pdf) $(dep)
	rm -f $(fuentes_aux) 

dvipdf:	$(fuentes:%.tex=%_dvipdf)
	rm -f $(fuentes_aux) 

%.pdf:	%.tex
	$(cc) $<
	$(cc) $<

%.dvi:	%.tex
	$(latex) $<
	$(latex) $<

%_dvipdf: %.dvi
	dvipdf $<
	rm -f $< 

clean:
	rm -f $(fuentes:%.tex=%.pdf) $(fuentes:%.tex=%.dvi)


# dep = conf/comandos.tex conf/config.tex conf/fuentes.tex \
# conf/packages.tex conf/preconfig.tex
# aux = $(fuente:%.tex=%.aux) $(fuente:%.tex=%.log) $(fuente:%.tex=%.out) \
# $(dep:%.tex=%.aux)
# pdfs = cv.pdf img/01.pdf img/02.pdf img/03.pdf img/04.pdf img/05.pdf \
# img/06.pdf img/07.pdf img/08.pdf letter.pdf
# # 'compilador':
# cc = pdflatex -interaction nonstopmode
# latex = latex

# all : pdflatex

# pdflatex : $(fuente) $(dep)
# 	$(cc) $(fuente)
# 	$(cc) $(fuente)
# 	rm -f $(aux) 

# latex : $(fuente) $(dep)
# 	$(latex) $(fuente)
# 	$(latex) $(fuente)
# 	dvipdf $(fuente:%.tex=%.dvi)
# 	rm -f $(fuente:%.tex=%.dvi) $(aux)

# clean:
# 	rm -f $(fuente:%.tex=%.pdf) $(fuente:%.tex=%.dvi)