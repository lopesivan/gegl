SLICE_X     = 10
SLICE_Y     = 10
SLICE_WIDTH = 150
SLICE_HEIGHT= 200

OUT =\
	gegl-slicer rules-01.txt slice-01.png \
	slice-02.png slice-03.png slice-04.png slice-05.png \
	rules-01.txt rules-02.txt rules-03.txt rules-04.txt rules-05.txt \
	2geglbuffer csugar float-lookup geglbuffer-add-image geglbuffer-clock gegl-convert gegl-slicer hello-world hello-world-video

all: run-gegl-slicer

2geglbuffer: 2geglbuffer.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

csugar: csugar.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

float-lookup: float-lookup.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

geglbuffer-add-image: geglbuffer-add-image.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

hello-world-video: hello-world-video.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

geglbuffer-clock: geglbuffer-clock.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@


#./gegl-convert a.png b.jpg
gegl-convert: gegl-convert.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

hello-world: hello-world.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

gegl-slicer: gegl-slicer.c
	gcc $^ `pkg-config --libs --cflags gegl-0.2 gthread-2.0` -o $@

rules-01.txt:
	@echo X Y width x height width slice1.png
	@echo $(SLICE_X) $(SLICE_Y) $(SLICE_WIDTH) $(SLICE_HEIGHT) slice-01.png
	@echo $(SLICE_X) $(SLICE_Y) $(SLICE_WIDTH)x$(SLICE_HEIGHT) slice-01.png > $@

run-gegl-slicer-01: gegl-slicer rules-01.txt
	@file a.png
	./gegl-slicer a.png  rules-01.txt ./
	@file slice-01.png

rules-02.txt:
	@echo X Y width x height width
	@echo 0   0 128x257 slice-02.png
	@echo 0   0 128x257 slice-02.png > $@

run-gegl-slicer-02: gegl-slicer rules-02.txt
	@file a.png
	./gegl-slicer a.png  rules-02.txt ./
	@file slice-02.png

rules-03.txt:
	@echo X Y width x height width
	@echo 128 0 128x257 slice-03.png
	@echo 128 0 128x257 slice-03.png > $@

run-gegl-slicer-03: gegl-slicer rules-03.txt
	@file a.png
	./gegl-slicer a.png  rules-03.txt ./
	@file slice-03.png

rules-04.txt:
	@echo X Y width x height width
	@echo 257 0 128x257 slice-04.png
	@echo 257 0 128x257 slice-04.png > $@

run-gegl-slicer-04: gegl-slicer rules-04.txt
	@file a.png
	./gegl-slicer a.png  rules-04.txt ./
	@file slice-04.png

rules-05.txt:
	@echo X Y width x height width
	@echo 384 0 128x257 slice-05.png
	@echo 384 0 128x257 slice-05.png > $@

run-gegl-slicer-05: gegl-slicer rules-05.txt
	@file a.png
	./gegl-slicer a.png  rules-05.txt ./
	@file slice-05.png

# ============================================================================
# ============================================================================
# ============================================================================

run-gegl-slicer: run-gegl-slicer-01 run-gegl-slicer-02 run-gegl-slicer-03 run-gegl-slicer-04 run-gegl-slicer-05

clean:
	rm -rf $(OUT)

