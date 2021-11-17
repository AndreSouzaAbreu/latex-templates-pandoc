PREFIX=example-
TEMPLATE_1=college-assignment
TEMPLATE_2=college-assignment-titlepage
TEMPLATE_3=college-report

all:
	@for i in {1..3}; do make example$$i; done

${PREFIX}${TEMPLATE_1}.pdf: ${PREFIX}${TEMPLATE_1}.md
	pandoc --pdf-engine=xelatex --template ${TEMPLATE_1} --output $@ $<

${PREFIX}${TEMPLATE_2}.pdf: ${PREFIX}${TEMPLATE_2}.md
	pandoc --pdf-engine=xelatex --template ${TEMPLATE_2} --output $@ $<

${PREFIX}${TEMPLATE_3}.pdf: ${PREFIX}${TEMPLATE_3}.md
	pandoc --pdf-engine=xelatex --template ${TEMPLATE_3} --output $@ $<

# shortcuts

example1: ${PREFIX}${TEMPLATE_1}.pdf
example2: ${PREFIX}${TEMPLATE_2}.pdf
example3: ${PREFIX}${TEMPLATE_3}.pdf


clean:
	-rm -f *.pdf

.PHONY: example1 example2 example3 clean
