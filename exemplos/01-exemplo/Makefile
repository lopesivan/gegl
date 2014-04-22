TARGETS=\
clones.png                 \
composite-transform.png    \
edge-laplace-broken.png    \
edge-sobel.png             \
exemplo-01.png             \
exemplo-02.png             \
fattal02.png               \
gamma-broken.png           \
hdr-color.png              \
jp2-load.png               \
a-load.png                 \
b-load.png                 \
mantiuk06.png              \
matting-global.png         \
matting-levin.png          \
pixelize.png               \
reflect2.png               \
reflect.png                \
reinhard05.png             \
rgbe-load.png              \
rgbe-save.png              \
rgb-params.png             \
rotate.png                 \
simple-scale.png           \
transform.png

OUT =\
a.png

all: $(TARGETS)

b-load.png: b-load.xml
	convert -size 200x200 xc:red a.png
	convert -size 400x400 xc:green b.png
	gegl $^ -o $@

a-load.png: a-load.xml
	convert -size 200x200 xc:red a.png
	gegl $^ -o $@

exemplo-01.png: composite-transform.xml
	convert -size 200x200 xc:red a.png
	gegl $^ -o $@

exemplo-02.png: exemplo-02.xml
	convert -size 200x200 xc:red a.png
	gegl $^ -o $@

edge-sobel.png: edge-sobel.xml
	gegl $^ -o $@

clones.png: clones.xml
	convert -size 200x200 xc:red a.png
	gegl $^ -o $@

composite-transform.png:composite-transform.xml
	gegl $^ -o $@

edge-laplace-broken.png:edge-laplace-broken.xml
	gegl $^ -o $@

fattal02.png:fattal02.xml
	gegl $^ -o $@

gamma-broken.png:gamma-broken.xml
	gegl $^ -o $@

hdr-color.png:hdr-color.xml
	gegl $^ -o $@

jp2-load.png:jp2-load.xml
	gegl $^ -o $@

mantiuk06.png:mantiuk06.xml
	gegl $^ -o $@

matting-global.png:matting-global.xml
	gegl $^ -o $@

matting-levin.png:matting-levin.xml
	gegl $^ -o $@

pixelize.png:pixelize.xml
	gegl $^ -o $@

reflect2.png:reflect2.xml
	gegl $^ -o $@

reflect.png:reflect.xml
	gegl $^ -o $@

reinhard05.png:reinhard05.xml
	gegl $^ -o $@

rgbe-load.png:rgbe-load.xml
	gegl $^ -o $@

rgbe-save.png:rgbe-save.xml
	gegl $^ -o $@

rgb-params.png:rgb-params.xml
	gegl $^ -o $@

rotate.png:rotate.xml
	gegl $^ -o $@

simple-scale.png:simple-scale.xml
	gegl $^ -o $@

transform.png:transform.xml
	gegl $^ -o $@

clean:
	@rm -rf $(TARGETS) $(OUT)

#EOF

