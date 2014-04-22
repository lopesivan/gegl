all: test

test:test.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

run: test
	@./test

clean:
	@rm test output_save.png
