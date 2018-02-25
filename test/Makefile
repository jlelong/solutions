all: test_after.pdf test_inline.pdf  test_nosol.pdf  test_separate.pdf

FILES=test_after test_inline test_nosol test_separate

%.pdf: %.tex
	latexmk $<


clean:
	@echo "cleaning all temporrary files"
	@for f in ${FILES}; \
	do \
		latexmk -C $${f};\
	done