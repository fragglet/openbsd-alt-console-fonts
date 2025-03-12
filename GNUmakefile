
FONTS = \
    dejavu16.bin \
    dejavu24.bin \
    dejavu32.bin \
    fira16.bin \
    fira24.bin \
    gomono16.bin \
    gomono24.bin

all: $(FONTS)

%.bin: txt/%.txt
	./mkfont $^ $@

clean:
	rm -f $(FONTS)
