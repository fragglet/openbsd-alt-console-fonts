
FONTS = \
    dejavu16.bin \
    dejavu24.bin \
    dejavu32.bin

all: $(FONTS)

%.bin: txt/%.txt
	./mkfont $^ $@

clean:
	rm -f $(FONTS)
