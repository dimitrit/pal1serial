objects = hello.pap 

default: all

%.pap: %.obj
	srec_cat $< -output $@ -MOS_Technologies -CRLF

%.obj: %.a65
	64tass -a -q --s-record $< -o $@ -m -L $(basename $<).lst --verbose-list

all: $(objects)

clean:
	@rm -f *.lst *.img *.com *.bin *.obj *.pap

.PHONY: clean debug test
