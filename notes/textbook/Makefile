.PHONY: all clean clobber

all: pdf/degn-notes.pdf pdf/degn-ch1-notes.pdf pdf/degn-ch2-notes.pdf

# this target needs to be fixed to work in all
# it only works when explicitly called for some reason,
# i.e. I cannot put the % in all, I have to list each one
pdf/degn-ch%-notes.pdf: tex/degn-ch%-notes.tex pdf
	pdflatex -output-directory pdf $< && \
	pdflatex -output-directory pdf $<

pdf/degn-notes.pdf: degn-notes.tex pdf
	pdflatex -output-directory pdf $< && \
	pdflatex -output-directory pdf $<

pdf:
	mkdir pdf

clean:
	rm -rf pdf/*.aux pdf/*.log pdf/*.toc

clobber: clean
	rm -rf pdf
