all: compile

compile:
	tiddlywiki site --savetiddlers [is[image]] images
	tiddlywiki site --setfield [is[image]] _canonical_uri $$:/core/templates/canonical-uri-external-image text/plain
	tiddlywiki site --setfield [is[image]] text "" text/plain
	tiddlywiki site --build index
	mv site/output/index.html ../wiki.html
	mv site/output/images/* ../images/

server:
	tiddlywiki site --listen

