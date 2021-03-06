# Zen Coding snippets for CSS

Copyright © 2008–2012 Vadim Makeev, http://pepelsbey.net
Licensed under MIT license

- @rules
- Pseudo
- Positioning
- Block
- Dimensions
- Colors
- Content
- Text
- Visual
- Layout
- Document
- Special

## @rules

	@c
	@charset '${1:utf-8}';

	@n
	@namespace '$1';

	@i
	@import url($1);

	@m
	@media {
		$0
		}

	@m:a
	@media all and $1 {
		$0
		}

	@m:s
	@media screen and $1 {
		$0
		}

	@m:p
	@media print and $1 {
		$0
		}

	@f
	@font-face {
		font-family:$1;
		src:local($2), url($3) format($4);
		}

	@f+
	@font-face {
		font-family:${1:FontFamily};
		src:url(${2:font}.eot);
		src:local($1),
			url($2.eot?iefix) format('embedded-opentype'),
			url($2.woff) format('woff'),
			url($2.ttf) format('truetype'),
			url($2.svg#${3:FontName}) format('svg');
		}

	@k
	@keyframes ${1:name} {
		$0
		}

	@wk
	@-webkit-keyframes ${1:name} {
		$0
		}

	@mk
	@-moz-keyframes ${1:name} {
		$0
		}

	@msk
	@-ms-keyframes ${1:name} {
		$0
		}

	@ok
	@-o-keyframes ${1:name} {
		$0
		}

	@r
	@region {
		$0
		}

	@p
	@page {
		$0
		}

	@v
	@viewport {
		$0
		}

	@ov
	@-o-viewport {
		$0
		}

## Pseudo

	:r
	:root

	:fc
	:first-child

	:lc
	:last-child

	:ft
	:first-of-type

	:lt
	:last-of-type

	:oc
	:only-child

	:ot
	:only-of-type

	:em
	:empty

	:l
	:link

	:v
	:visited

	:a
	:active

	:h
	:hover

	:f
	:focus

	:t
	:target

	:en
	:enabled

	:di
	:disabled

	:ch
	:checked

	:fli
	:first-line

	:fle
	:first-letter

	:be
	:before

	:af
	:after

	:la
	:lang($1)

	:nc
	:nth-child($1)

	:nlc
	:nth-last-child($1)

	:nt
	:nth-of-type($1)

	:nlt
	:nth-last-of-type($1)

	:n
	:not($1)

	:s
	::selection

	:ms
	::-moz-selection

## Positioning

	pos
	position:$1;

	pos:s
	position:static;

	pos:a
	position:absolute;

	pos:r
	position:relative;

	pos:f
	position:fixed;

	t
	top:${1:0};

	t:a
	top:auto;

	r
	right:${1:0};

	r:a
	right:auto;

	b
	bottom:${1:0};

	b:a
	bottom:auto;

	l
	left:${1:0};

	l:a
	left:auto;

	z
	z-index:${1:1};

	z:a
	z-index:auto;

	## Block

	fl
	float:$1;

	fl:n
	float:none;

	fl:l
	float:left;

	fl:r
	float:right;

	cl
	clear:$1;

	cl:n
	clear:none;

	cl:l
	clear:left;

	cl:r
	clear:right;

	cl:b
	clear:both;

	d
	display:$1;

	d:n
	display:none;

	d:i
	display:inline;

	d:b
	display:block;

	d:ib
	display:inline-block;

	d:li
	display:list-item;

	d:ri
	display:run-in;

	d:c
	display:compact;

	d:f
	display:flexbox;

	d:if
	display:inline-flexbox;

	d:it
	display:inline-table;

	d:tca
	display:table-caption;

	d:tco
	display:table-column;

	d:tcg
	display:table-column-group;

	d:thg
	display:table-header-group;

	d:tfg
	display:table-footer-group;

	d:tr
	display:table-row;

	d:trg
	display:table-row-group;

	d:tc
	display:table-cell;

	v
	visibility:$1;

	v:v
	visibility:visible;

	v:h
	visibility:hidden;

	v:c
	visibility:collapse;

	ov
	overflow:$1;

	ov:v
	overflow:visible;

	ov:h
	overflow:hidden;

	ov:s
	overflow:scroll;

	ov:a
	overflow:auto;

	ovx
	overflow-x:$1;

	ovx:v
	overflow-x:visible;

	ovx:h
	overflow-x:hidden;

	ovx:s
	overflow-x:scroll;

	ovx:a
	overflow-x:auto;

	ovy
	overflow-y:$1;

	ovy:v
	overflow-y:visible;

	ovy:h
	overflow-y:hidden;

	ovy:s
	overflow-y:scroll;

	ovy:a
	overflow-y:auto;

	msovx
	-ms-overflow-x:$1;

	msovy
	-ms-overflow-y:$1;

	cp
	clip:rect(${1:0}, ${2:0}, ${3:0}, ${4:0});

	cp:a
	clip:auto;

	bs
	box-sizing:$1;

	bs:cb
	box-sizing:content-box;

	bs:bb
	box-sizing:border-box;

	fxd
	flex-direction:$1;

	fxd:lr
	flex-direction:lr;

	fxd:rl
	flex-direction:rl;

	fxd:tb
	flex-direction:tb;

	fxd:bt
	flex-direction:bt;

	fxd:i
	flex-direction:inline;

	fxd:ir
	flex-direction:inline-reverse;

	fxd:b
	flex-direction:block;

	fxd:br
	flex-direction:block-reverse;

	fxo
	flex-order:$1;

	fxp
	flex-pack:$1;

	fxp:s
	flex-pack:start;

	fxp:e
	flex-pack:end;

	fxp:c
	flex-pack:center;

	fxp:j
	flex-pack:justify;

	fxa
	flex-align:$1;

	fxa:a
	flex-align:auto;

	fxa:b
	flex-align:baseline;

## Dimensions

	m
	margin:${1:0};

	m:a
	margin:auto;

	mt
	margin-top:${1:0};

	mt:a
	margin-top:auto;

	mr
	margin-right:${1:0};

	mr:a
	margin-right:auto;

	mb
	margin-bottom:${1:0};

	mb:a
	margin-bottom:auto;

	ml
	margin-left:${1:0};

	ml:a
	margin-left:auto;

	p
	padding:${1:0};

	pt
	padding-top:${1:0};

	pr
	padding-right:${1:0};

	pb
	padding-bottom:${1:0};

	pl
	padding-left:${1:0};

	miw
	min-width:${1:0};

	mih
	min-height:${1:0};

	maw
	max-width:${1:0};

	maw:n
	max-width:none;

	mah
	max-height:${1:0};

	mah:n
	max-height:none;

	w
	width:${1:0};

	w:a
	width:auto;

	w:dw
	width:device-width;

	h
	height:${1:0};

	h:a
	height:auto;

	h:dh
	height:device-height;

## Colors

	o
	outline:$1;

	o+
	outline:${1:1px} ${2:dotted} ${3:#000};

	o:n
	outline:none;

	ow
	outline-width:${1:1px};

	os
	outline-style:${1:dotted};

	os:n
	outline-style:none;

	oc
	outline-color:${1:#000};

	oc:i
	outline-color:invert;

	oo
	outline-offset:${1:0};

	bd
	border:$1;

	bd+
	border:${1:1px} ${2:solid} ${3:#000};

	bd:n
	border:none;

	bdcl
	border-collapse:$1;

	bdcl:c
	border-collapse:collapse;

	bdcl:s
	border-collapse:separate;

	bdsp
	border-spacing:$1;

	bdw
	border-width:${1:1px};

	bds
	border-style:$1;

	bds:n
	border-style:none;

	bds:h
	border-style:hidden;

	bds:dt
	border-style:dotted;

	bds:ds
	border-style:dashed;

	bds:s
	border-style:solid;

	bds:db
	border-style:double;

	bds:g
	border-style:groove;

	bds:r
	border-style:ridge;

	bds:i
	border-style:inset;

	bds:o
	border-style:outset;

	bdc
	border-color:${1:#000};

	bdt
	border-top:$1;

	bdt+
	border-top:${1:1px} ${2:solid} ${3:#000};

	bdt:n
	border-top:none;

	bdtw
	border-top-width:${1:1px};

	bdts
	border-top-style:${1:solid};

	bdts:n
	border-top-style:none;

	bdtc
	border-top-color:${1:#000};

	bdr
	border-right:$1;

	bdr+
	border-right:${1:1px} ${2:solid} ${3:#000};

	bdr:n
	border-right:none;

	bdrw
	border-right-width:${1:1px};

	bdrs
	border-right-style:${1:solid};

	bdrs:n
	border-right-style:none;

	bdrc
	border-right-color:${1:#000};

	bdb
	border-bottom:$1;

	bdb+
	border-bottom:${1:1px} ${2:solid} ${3:#000};

	bdb:n
	border-bottom:none;

	bdbw
	border-bottom-width:${1:1px};

	bdbs
	border-bottom-style:${1:solid};

	bdbs:n
	border-bottom-style:none;

	bdbc
	border-bottom-color:${1:#000};

	bdl
	border-left:$1;

	bdl+
	border-left:${1:1px} ${2:solid} ${3:#000};

	bdl:n
	border-left:none;

	bdlw
	border-left-width:${1:1px};

	bdls
	border-left-style:${1:solid};

	bdls:n
	border-left-style:none;

	bdlc
	border-left-color:${1:#000};

	bdrz
	-webkit-border-radius:${1:0};
	-moz-border-radius:$1;
	border-radius:$1;

	bdtlrz
	-webkit-border-top-left-radius:${1:0};
	-moz-border-radius-topleft:$1;
	border-top-left-radius:$1;

	bdtrrz
	-webkit-border-top-right-radius:${1:0};
	-moz-border-radius-topright:$1;
	border-top-right-radius:$1;

	bdbrrz
	-webkit-border-bottom-right-radius:${1:0};
	-moz-border-radius-bottomright:$1;
	border-bottom-right-radius:$1;

	bdblrz
	-webkit-border-bottom-left-radius:${1:0};
	-moz-border-radius-bottomleft:$1;
	border-bottom-left-radius:$1;

	bdi
	-webkit-border-image:$1;
	-moz-border-image:$1;
	-o-border-image:$1;
	border-image:$1;

	bdi+
	-webkit-border-image:url($1) ${2:0} ${3:repeat};
	-moz-border-image:url($1) $2 $3;
	-o-border-image:url($1) $2 $3;
	border-image:url($1) $2 $3;

	bdi:n
	-webkit-border-image:none;
	-moz-border-image:none;
	-o-border-image:none;
	border-image:none;

	bdti
	-webkit-border-top-image:url($1);
	-moz-border-top-image:url($1);
	-o-border-top-image:url($1);
	border-top-image:url($1);

	bdri
	-webkit-border-right-image:url($1);
	-moz-border-right-image:url($1);
	-o-border-right-image:url($1);
	border-right-image:url($1);

	bdbi
	-webkit-border-bottom-image:url($1);
	-moz-border-bottom-image:url($1);
	-o-border-bottom-image:url($1);
	border-bottom-image:url($1);

	bdli
	-webkit-border-left-image:url($1);
	-moz-border-left-image:url($1);
	-o-border-left-image:url($1);
	border-left-image:url($1);

	bdci
	-webkit-border-corner-image:url($1);
	-moz-border-corner-image:url($1);
	-o-border-corner-image:url($1);
	border-corner-image:url($1);

	bdtli
	-webkit-border-top-left-image:url($1);
	-moz-border-top-left-image:url($1);
	-o-border-top-left-image:url($1);
	border-top-left-image:url($1);

	bdtri
	-webkit-border-top-right-image:url($1);
	-moz-border-top-right-image:url($1);
	-o-border-top-right-image:url($1);
	border-top-right-image:url($1);

	bdbri
	-webkit-border-bottom-right-image:url($1);
	-moz-border-bottom-right-image:url($1);
	-o-border-bottom-right-image:url($1);
	border-bottom-right-image:url($1);

	bdbli
	-webkit-border-bottom-left-image:url($1);
	-moz-border-bottom-left-image:url($1);
	-o-border-bottom-left-image:url($1);
	border-bottom-left-image:url($1);

	bdisr
	-webkit-border-image-source:url($1);
	-moz-border-image-source:url($1);
	-o-border-image-source:url($1);
	border-image-source:url($1);

	bdisr:n
	-webkit-border-image-source:none;
	-moz-border-image-source:none;
	-o-border-image-source:none;
	border-image-source:none;

	bdisl
	-webkit-border-image-slice:${1:0};
	-moz-border-image-slice:${1:0};
	-o-border-image-slice:${1:0};
	border-image-slice:${1:0};

	bdisl:f
	-webkit-border-image-slice:fill;
	-moz-border-image-slice:fill;
	-o-border-image-slice:fill;
	border-image-slice:fill;

	bdiw
	-webkit-border-image-width:${1:0};
	-moz-border-image-width:${1:0};
	-o-border-image-width:${1:0};
	border-image-width:${1:0};

	bdiw:a
	-webkit-border-image-width:auto;
	-moz-border-image-width:auto;
	-o-border-image-width:auto;
	border-image-width:auto;

	bdio
	-webkit-border-image-outset:${1:0};
	-moz-border-image-outset:${1:0};
	-o-border-image-outset:${1:0};
	border-image-outset:${1:0};

	bdir
	-webkit-border-image-repeat:$1;
	-moz-border-image-repeat:$1;
	-o-border-image-repeat:$1;
	border-image-repeat:$1;

	bdir:st
	-webkit-border-image-repeat:stretch;
	-moz-border-image-repeat:stretch;
	-o-border-image-repeat:stretch;
	border-image-repeat:stretch;

	bdir:re
	-webkit-border-image-repeat:repeat;
	-moz-border-image-repeat:repeat;
	-o-border-image-repeat:repeat;
	border-image-repeat:repeat;

	bdir:ro
	-webkit-border-image-repeat:round;
	-moz-border-image-repeat:round;
	-o-border-image-repeat:round;
	border-image-repeat:round;

	bdir:sp
	-webkit-border-image-repeat:space;
	-moz-border-image-repeat:space;
	-o-border-image-repeat:space;
	border-image-repeat:space;

	bg
	background:$1;

	bg+
	background:${1:#FFF} url($2) ${3:0} ${4:0} ${5:no-repeat};

	bg:n
	background:none;

	iefbg
	filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(src='$1', sizingMethod='${2:crop}');

	bgc
	background-color:${1:#FFF};

	bgc:t
	background-color:transparent;

	bgi
	background-image:${1:url($2)};

	bgi:n
	background-image:none;

	bgi:lg
	background-image:-webkit-linear-gradient(${1:top}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%});
	background-image:-moz-linear-gradient($1, $2 $3, $4 $5);
	background-image:-ms-linear-gradient($1, $2 $3, $4 $5);
	background-image:-o-linear-gradient($1, $2 $3, $4 $5);
	background-image:linear-gradient($1, $2 $3, $4 $5);

	bgi:rlg
	background-image:-webkit-repeating-linear-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%});
	background-image:-moz-repeating-linear-gradient($1, $2 $3, $4 $5);
	background-image:-ms-repeating-linear-gradient($1, $2 $3, $4 $5);
	background-image:-o-repeating-linear-gradient($1, $2 $3, $4 $5);
	background-image:repeating-linear-gradient($1, $2 $3, $4 $5);

	bgi:rg
	background-image:-webkit-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:100%});
	background-image:-moz-radial-gradient($1, $2 $3, $4 $5);
	background-image:-ms-radial-gradient($1, $2 $3, $4 $5);
	background-image:-o-radial-gradient($1, $2 $3, $4 $5);
	background-image:radial-gradient($1, $2 $3, $4 $5);

	bgi:rrg
	background-image:-webkit-repeating-radial-gradient(${1:center}, ${2:#000} ${3:0}, ${4:#FFF} ${5:25%});
	background-image:-moz-repeating-radial-gradient($1, $2 $3, $4 $5);
	background-image:-ms-repeating-radial-gradient($1, $2 $3, $4 $5);
	background-image:-o-repeating-radial-gradient($1, $2 $3, $4 $5);
	background-image:repeating-radial-gradient($1, $2 $3, $4 $5);

	bgr
	background-repeat:$1;

	bgr:r
	background-repeat:repeat;

	bgr:x
	background-repeat:repeat-x;

	bgr:y
	background-repeat:repeat-y;

	bgr:sp
	background-repeat:space;

	bgr:ro
	background-repeat:round;

	bgr:n
	background-repeat:no-repeat;

	bga
	background-attachment:$1;

	bga:f
	background-attachment:fixed;

	bga:l
	background-attachment:local;

	bga:s
	background-attachment:scroll;

	bgp
	background-position:${1:0} ${2:0};

	bgpx
	background-position-x:$1;

	msbgpx
	-ms-background-position-x:$1;

	bgpy
	background-position-y:$1;

	msbgpy
	-ms-background-position-y:$1;

	bgcp
	background-clip:$1;

	bgcp:bb
	background-clip:border-box;

	bgcp:pb
	background-clip:padding-box;

	bgcp:cb
	background-clip:content-box;

	bgo
	background-origin:$1;

	bgo:pb
	background-origin:padding-box;

	bgo:bb
	background-origin:border-box;

	bgo:cb
	background-origin:content-box;

	bgz
	-webkit-background-size:$1;
	-moz-background-size:$1;
	background-size:$1;

	bgz:a
	background-size:auto;

	bgz:con
	background-size:contain;

	bgz:cov
	background-size:cover;

	bdbr
	box-decoration-break:$1;

	bdbr:s
	box-decoration-break:slice;

	bdbr:c
	box-decoration-break:clone;

	bsh
	-webkit-box-shadow:$1;
	-moz-box-shadow:$1;
	box-shadow:$1;

	bsh+
	-webkit-box-shadow:${1:0} ${2:0} ${3:0} ${4:#000};
	-moz-box-shadow:$1 $2 $3 $4;
	box-shadow:$1 $2 $3 $4;

	bsh:i
	-webkit-box-shadow:${1:0} ${2:0} ${3:0} ${4:#000} ${5:inset};
	-moz-box-shadow:$1 $2 $3 $4 $5;
	box-shadow:$1 $2 $3 $4 $5;

	bsh:n
	-webkit-box-shadow:none;
	-moz-box-shadow:none;
	box-shadow:none;

	c
	color:${1:#000};

	lg
	linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	wlg
	-webkit-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	mlg
	-moz-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	mslg
	-ms-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	olg
	-o-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	ieflg
	filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=${1:#FF000000}, endColorstr=${2:#FFFFFFFF});

	msflg
	-ms-filter:'progid:DXImageTransform.Microsoft.gradient(startColorstr=${1:#FF000000}, endColorstr=${2:#FFFFFFFF});

	rlg
	repeating-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	wrlg
	-webkit-repeating-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	mrlg
	-moz-repeating-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	msrlg
	-ms-repeating-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	orlg
	-o-repeating-linear-gradient(${1:${2:top}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	rg
	radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	wrg
	-webkit-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	mrg
	-moz-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	msrg
	-ms-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	org
	-o-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:100%}})

	rrg
	repeating-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	wrrg
	-webkit-repeating-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	mrrg
	-moz-repeating-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	msrrg
	-ms-repeating-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	orrg
	-o-repeating-radial-gradient(${1:${2:center}, ${3:#000} ${4:0}, ${5:#FFF} ${6:25%}})

	rgb
	rgb(${1:0}, ${2:0}, ${3:0})

	rgba
	rgba(${1:0}, ${2:0}, ${3:0}, ${4:1})

	hsl
	hsl(${1:0}, ${2:0}, ${3:0})

	hsla
	hsla(${1:0}, ${2:0}, ${3:0}, ${4:1})

	u
	url($1)

## Content

	tl
	table-layout:$1;

	tl:a
	table-layout:auto;

	tl:f
	table-layout:fixed;

	cs
	caption-side:$1;

	cs:t
	caption-side:top;

	cs:b
	caption-side:bottom;

	ec
	empty-cells:$1;

	ec:s
	empty-cells:show;

	ec:h
	empty-cells:hide;

	ls
	list-style:$1;

	ls:n
	list-style:none;

	lsp
	list-style-position:$1;

	lsp:i
	list-style-position:inside;

	lsp:o
	list-style-position:outside;

	lst
	list-style-type:$1;

	lst:n
	list-style-type:none;

	lst:d
	list-style-type:disc;

	lst:c
	list-style-type:circle;

	lst:s
	list-style-type:square;

	lst:dc
	list-style-type:decimal;

	lst:dclz
	list-style-type:decimal-leading-zero;

	lst:lr
	list-style-type:lower-roman;

	lst:ur
	list-style-type:upper-roman;

	lsi
	list-style-image:${1:url($2)};

	lsi:n
	list-style-image:none;

	q
	quotes:$1;

	q:n
	quotes:none;

	q:en
	quotes:'\201C' '\201D' '\2018' '\2019';

	q:ru
	quotes:'\00AB' '\00BB' '\201E' '\201C';

	ct
	content:$1;

	ct:n
	content:normal;

	ct:oq
	content:open-quote;

	ct:noq
	content:no-open-quote;

	ct:cq
	content:close-quote;

	ct:ncq
	content:no-close-quote;

	ct:a
	content:attr($1);

	ct:co
	content:counter($1);

	ct:cs
	content:counters($1);

	ct:i
	content:icon;

	ci
	counter-increment:$1;

	cr
	counter-reset:$1;

	## Text

	mswm
	-ms-writing-mode:$1;

	va
	vertical-align:$1;

	va:sup
	vertical-align:super;

	va:t
	vertical-align:top;

	va:tt
	vertical-align:text-top;

	va:m
	vertical-align:middle;

	va:ba
	vertical-align:baseline;

	va:bo
	vertical-align:bottom;

	va:tb
	vertical-align:text-bottom;

	va:sub
	vertical-align:sub;

	ta
	text-align:$1;

	ta:l
	text-align:left;

	ta:c
	text-align:center;

	ta:r
	text-align:right;

	ta:j
	text-align:justify;

	ta:s
	text-align:start;

	ta:e
	text-align:end;

	tal
	text-align-last:$1;

	mstal
	-ms-text-align-last:$1;

	tal:a
	text-align-last:auto;

	tal:l
	text-align-last:left;

	tal:c
	text-align-last:center;

	tal:r
	text-align-last:right;

	tal:j
	text-align-last:justify;

	td
	text-decoration:$1;

	td:n
	text-decoration:none;

	td:o
	text-decoration:overline;

	td:lt
	text-decoration:line-through;

	td:u
	text-decoration:underline;

	te
	text-emphasis:$1;

	tec
	text-emphasis-color:${1:#C00};

	tes
	text-emphasis-style:$1;

	tep
	text-emphasis-position:$1;

	ti
	text-indent:$1;

	ti:el
	text-indent:each-line;

	ti:h
	text-indent:hanging;

	ti:-
	text-indent:-9999px;

	tj
	text-justify:$1;

	mstj
	-ms-text-justify:$1;

	tj:a
	text-justify:auto;

	tj:iw
	text-justify:inter-word;

	tj:ii
	text-justify:inter-ideograph;

	tj:ic
	text-justify:inter-cluster;

	tj:d
	text-justify:distribute;

	tj:dal
	text-justify:distribute-all-lines;

	tj:dcl
	text-justify:distribute-center-last;

	tj:k
	text-justify:kashida;

	tj:n
	text-justify:newspaper;

	tj:t
	text-justify:tibetan;

	to
	text-outline:$1;

	to+
	text-outline:${1:0} ${2:0} ${3:#000};

	to:n
	text-outline:none;

	tt
	text-transform:$1;

	tt:n
	text-transform:none;

	tt:c
	text-transform:capitalize;

	tt:u
	text-transform:uppercase;

	tt:l
	text-transform:lowercase;

	tt:f
	text-transform:fullwidth;

	tw
	text-wrap:$1;

	tw:n
	text-wrap:normal;

	tw:no
	text-wrap:none;

	tw:u
	text-wrap:unrestricted;

	tw:a
	text-wrap:avoid;

	tov
	text-overflow:$1;

	mstov
	-ms-text-overflow:$1;

	tove
	text-overflow-ellipsis:$1;

	tovm
	text-overflow-mode:$1;

	tovm:c
	text-overflow-mode:clip;

	tovm:e
	text-overflow-mode:ellipsis;

	tovm:ew
	text-overflow-mode:ellipsis-word;

	tsh
	text-shadow:$1;

	tsh+
	text-shadow:${1:0} ${2:0} ${3:0} ${4:#000};

	tsh:n
	text-shadow:none;

	lh
	line-height:${1:1};

	lh:n
	line-height:normal;

	whs
	white-space:$1;

	whs:n
	white-space:normal;

	whs:p
	white-space:pre;

	whs:nw
	white-space:nowrap;

	whs:pw
	white-space:pre-wrap;

	whs:pl
	white-space:pre-line;

	wos
	word-spacing:$1;

	wos:n
	word-spacing:normal;

	wow
	word-wrap:$1;

	mswow
	-ms-word-wrap:$1;

	wow:n
	word-wrap:normal;

	wow:bw
	word-wrap:break-word;

	wob
	word-break:$1;

	mswob
	-ms-word-break:$1;

	ts
	-moz-tab-size:$1;
	-o-tab-size:$1;
	tab-size:$1;

	hy
	-webkit-hyphens:$1;
	-moz-hyphens:$1;
	hyphens:$1;

	hy:n
	-webkit-hyphens:none;
	-moz-hyphens:none;
	hyphens:none;

	hy:m
	-webkit-hyphens:manual;
	-moz-hyphens:manual;
	hyphens:manual;

	hy:a
	-webkit-hyphens:auto;
	-moz-hyphens:auto;
	hyphens:auto;

	les
	letter-spacing:$1;

	les:n
	letter-spacing:normal;

	f
	font:$1;

	f+
	font:${1:1em} ${2:Arial}, ${3:sans-serif};

	fw
	font-weight:$1;

	fw:n
	font-weight:normal;

	fw:b
	font-weight:bold;

	fw:br
	font-weight:bolder;

	fw:lr
	font-weight:lighter;

	fw:1
	font-weight:100;

	fw:2
	font-weight:200;

	fw:3
	font-weight:300;

	fw:4
	font-weight:400;

	fw:5
	font-weight:500;

	fw:6
	font-weight:600;

	fw:7
	font-weight:700;

	fw:8
	font-weight:800;

	fw:9
	font-weight:900;

	fs
	font-style:$1;

	fs:n
	font-style:normal;

	fs:i
	font-style:italic;

	fs:o
	font-style:oblique;

	fv
	font-variant:$1;

	fv:n
	font-variant:normal;

	fv:sc
	font-variant:small-caps;

	fza
	font-size-adjust:$1;

	fza:n
	font-size-adjust:none;

	fst
	font-stretch:$1;

	fst:n
	font-stretch:normal;

	fst:uc
	font-stretch:ultra-condensed;

	fst:ec
	font-stretch:extra-condensed;

	fst:c
	font-stretch:condensed;

	fst:sc
	font-stretch:semi-condensed;

	fst:se
	font-stretch:semi-expanded;

	fst:e
	font-stretch:expanded;

	fst:ee
	font-stretch:extra-expanded;

	fst:ue
	font-stretch:ultra-expanded;

	fz
	font-size:$1;

	ff
	font-family:$1;

	ff:s
	font-family:serif;

	ff:ss
	font-family:sans-serif;

	ff:c
	font-family:cursive;

	ff:f
	font-family:fantasy;

	ff:m
	font-family:monospace;

## Visual

	op
	opacity:$1;

	iefop
	filter:progid:DXImageTransform.Microsoft.Alpha(Opacity=${1:100});

	msfop
	-ms-filter:'progid:DXImageTransform.Microsoft.Alpha(Opacity=${1:100})';

	msim
	-ms-interpolation-mode:$1;

	msim:b
	-ms-interpolation-mode:bicubic;

	msim:n
	-ms-interpolation-mode:nearest-neighbor;

	fi
	filter:$1;

	wfi
	-webkit-filter:$1;

	rz
	resize:$1;

	rz:n
	resize:none;

	rz:b
	resize:both;

	rz:h
	resize:horizontal;

	rz:v
	resize:vertical;

	us
	-webkit-user-select:$1;
	-moz-user-select:$1;
	-ms-user-select:$1;
	user-select:$1;

	us:n
	-webkit-user-select:none;
	-moz-user-select:none;
	-ms-user-select:none;
	user-select:none;

	us:a
	-webkit-user-select:all;
	-moz-user-select:all;
	-ms-user-select:all;
	user-select:all;

	us:e
	-webkit-user-select:element;
	-moz-user-select:element;
	-ms-user-select:element;
	user-select:element;

	us:t
	-webkit-user-select:text;
	-moz-user-select:text;
	-ms-user-select:text;
	user-select:text;

	cur
	cursor:$1;

	cur:a
	cursor:auto;

	cur:d
	cursor:default;

	cur:n
	cursor:none;

	cur:cm
	cursor:context-menu;

	cur:h
	cursor:help;

	cur:p
	cursor:pointer;

	cur:pr
	cursor:progress;

	cur:w
	cursor:wait;

	cur:c
	cursor:cell;

	cur:cr
	cursor:crosshair;

	cur:t
	cursor:text;

	cur:vt
	cursor:vertical-text;

	cur:al
	cursor:alias;

	cur:cp
	cursor:copy;

	cur:mv
	cursor:move;

	cur:nd
	cursor:no-drop;

	cur:na
	cursor:not-allowed;

	cur:er
	cursor:e-resize;

	cur:nr
	cursor:n-resize;

	cur:ner
	cursor:ne-resize;

	cur:nwr
	cursor:nw-resize;

	cur:sr
	cursor:s-resize;

	cur:ser
	cursor:se-resize;

	cur:swr
	cursor:sw-resize;

	cur:wr
	cursor:w-resize;

	cur:ewr
	cursor:ew-resize;

	cur:nsr
	cursor:ns-resize;

	cur:neswr
	cursor:nesw-resize;

	cur:nwser
	cursor:nwse-resize;

	cur:cor
	cursor:col-resize;

	cur:ror
	cursor:row-resize;

	cur:als
	cursor:all-scroll;

	ni
	nav-index:$1;

	ni:a
	nav-index:auto;

	nu
	nav-up:$1;

	nu:a
	nav-up:auto;

	nr
	nav-right:$1;

	nr:a
	nav-right:auto;

	nd
	nav-down:$1;

	nd:a
	nav-down:auto;

	nl
	nav-left:$1;

	nl:a
	nav-left:auto;

	tr
	-webkit-transition:$1;
	-moz-transition:$1;
	-ms-transition:$1;
	-o-transition:$1;
	transition:$1;

	tr+
	-webkit-transition:${1:all} ${2:linear} ${3:1s};
	-moz-transition:$1 $2 $3;
	-ms-transition:$1 $2 $3;
	-o-transition:$1 $2 $3;
	transition:$1 $2 $3;

	tr:n
	-webkit-transition:none;
	-moz-transition:none;
	-ms-transition:none;
	-o-transition:none;
	transition:none;

	trde
	-webkit-transition-delay:${1:1s};
	-moz-transition-delay:$1;
	-ms-transition-delay:$1;
	-o-transition-delay:$1;
	transition-delay:$1;

	trtf
	-webkit-transition-timing-function:$1;
	-moz-transition-timing-function:$1;
	-ms-transition-timing-function:$1;
	-o-transition-timing-function:$1;
	transition-timing-function:$1;

	trtf:e
	-webkit-transition-timing-function:ease;
	-moz-transition-timing-function:ease;
	-ms-transition-timing-function:ease;
	-o-transition-timing-function:ease;
	transition-timing-function:ease;

	trtf:l
	-webkit-transition-timing-function:linear;
	-moz-transition-timing-function:linear;
	-ms-transition-timing-function:linear;
	-o-transition-timing-function:linear;
	transition-timing-function:linear;

	trtf:ei
	-webkit-transition-timing-function:ease-in;
	-moz-transition-timing-function:ease-in;
	-ms-transition-timing-function:ease-in;
	-o-transition-timing-function:ease-in;
	transition-timing-function:ease-in;

	trtf:eo
	-webkit-transition-timing-function:ease-out;
	-moz-transition-timing-function:ease-out;
	-ms-transition-timing-function:ease-out;
	-o-transition-timing-function:ease-out;
	transition-timing-function:ease-out;

	trtf:eio
	-webkit-transition-timing-function:ease-in-out;
	-moz-transition-timing-function:ease-in-out;
	-ms-transition-timing-function:ease-in-out;
	-o-transition-timing-function:ease-in-out;
	transition-timing-function:ease-in-out;

	trtf:cb
	-webkit-transition-timing-function:cubic-bezier(${1:0}, ${2:0}, ${3:0}, ${4:0});
	-moz-transition-timing-function:cubic-bezier($1, $2, $3, $4);
	-ms-transition-timing-function:cubic-bezier($1, $2, $3, $4);
	-o-transition-timing-function:cubic-bezier($1, $2, $3, $4);
	transition-timing-function:cubic-bezier($1, $2, $3, $4);

	trdu
	-webkit-transition-duration:${1:1s};
	-moz-transition-duration:$1;
	-ms-transition-duration:$1;
	-o-transition-duration:$1;
	transition-duration:$1;

	trp
	-webkit-transition-property:$1;
	-moz-transition-property:$1;
	-ms-transition-property:$1;
	-o-transition-property:$1;
	transition-property:$1;

	trp:a
	-webkit-transition-property:all;
	-moz-transition-property:all;
	-ms-transition-property:all;
	-o-transition-property:all;
	transition-property:all;

	trp:n
	-webkit-transition-property:none;
	-moz-transition-property:none;
	-ms-transition-property:none;
	-o-transition-property:none;
	transition-property:none;

	bv
	-webkit-backface-visibility:$1;
	-moz-backface-visibility:$1;
	-o-backface-visibility:$1;
	backface-visibility:$1;

	bv:v
	-webkit-backface-visibility:visible;
	-moz-backface-visibility:visible;
	-o-backface-visibility:visible;
	backface-visibility:visible;

	bv:h
	-webkit-backface-visibility:hidden;
	-moz-backface-visibility:hidden;
	-o-backface-visibility:hidden;
	backface-visibility:hidden;

	tf
	-webkit-transform:$1;
	-moz-transform:$1;
	-ms-transform:$1;
	-o-transform:$1;
	transform:$1;

	tf:n
	-webkit-transform:none;
	-moz-transform:none;
	-ms-transform:none;
	-o-transform:none;
	transform:none;

	tf:mx
	-webkit-transform:matrix(${1:0}, ${2:0}, ${3:0}, ${4:0}, ${5:0}, ${6:0});
	-moz-transform:matrix($1, $2, $3, $4, $5, $6);
	-ms-transform:matrix($1, $2, $3, $4, $5, $6);
	-o-transform:matrix($1, $2, $3, $4, $5, $6);
	transform:matrix($1, $2, $3, $4, $5, $6);

	tf:mx3
	-webkit-transform:matrix3d(${1:0}, ${2:0}, ${3:0}, ${4:0}, ${5:0}, ${6:0});
	-moz-transform:matrix3d($1, $2, $3, $4, $5, $6);
	-ms-transform:matrix3d($1, $2, $3, $4, $5, $6);
	-o-transform:matrix3d($1, $2, $3, $4, $5, $6);
	transform:matrix3d($1, $2, $3, $4, $5, $6);

	tf:per
	-webkit-transform:perspective(${1:0});
	-moz-transform:perspective($1);
	-ms-transform:perspective($1);
	-o-transform:perspective($1);
	transform:perspective($1);

	tf:rt
	-webkit-transform:rotate(${1:45deg});
	-moz-transform:rotate($1);
	-ms-transform:rotate($1);
	-o-transform:rotate($1);
	transform:rotate($1);

	tf:rtx
	-webkit-transform:rotateX(${1:45deg});
	-moz-transform:rotateX($1);
	-ms-transform:rotateX($1);
	-o-transform:rotateX($1);
	transform:rotateX($1);

	tf:rty
	-webkit-transform:rotateY(${1:45deg});
	-moz-transform:rotateY($1);
	-ms-transform:rotateY($1);
	-o-transform:rotateY($1);
	transform:rotateY($1);

	tf:rtz
	-webkit-transform:rotateZ(${1:45deg});
	-moz-transform:rotateZ($1);
	-ms-transform:rotateZ($1);
	-o-transform:rotateZ($1);
	transform:rotateZ($1);

	tf:sc
	-webkit-transform:scale(${1:0});
	-moz-transform:scale($1);
	-ms-transform:scale($1);
	-o-transform:scale($1);
	transform:scale($1);

	tf:scx
	-webkit-transform:scaleX(${1:0});
	-moz-transform:scaleX($1);
	-ms-transform:scaleX($1);
	-o-transform:scaleX($1);
	transform:scaleX($1);

	tf:scy
	-webkit-transform:scaleY(${1:0});
	-moz-transform:scaleY($1);
	-ms-transform:scaleY($1);
	-o-transform:scaleY($1);
	transform:scaleY($1);

	tf:scz
	-webkit-transform:scaleZ(${1:0});
	-moz-transform:scaleZ($1);
	-ms-transform:scaleZ($1);
	-o-transform:scaleZ($1);
	transform:scaleZ($1);

	tf:sk
	-webkit-transform:skew(${1:45deg});
	-moz-transform:skew($1);
	-ms-transform:skew($1);
	-o-transform:skew($1);
	transform:skew($1);

	tf:skx
	-webkit-transform:skewX(${1:45deg});
	-moz-transform:skewX($1);
	-ms-transform:skewX($1);
	-o-transform:skewX($1);
	transform:skewX($1);

	tf:sky
	-webkit-transform:skewY(${1:45deg});
	-moz-transform:skewY($1);
	-ms-transform:skewY($1);
	-o-transform:skewY($1);
	transform:skewY($1);

	tf:tl
	-webkit-transform:translate(${1:0}, ${2:0});
	-moz-transform:translate($1, $2);
	-ms-transform:translate($1, $2);
	-o-transform:translate($1, $2);
	transform:translate($1, $2);

	tf:tlx
	-webkit-transform:translateX(${1:0});
	-moz-transform:translateX($1);
	-ms-transform:translateX($1);
	-o-transform:translateX($1);
	transform:translateX($1);

	tf:tly
	-webkit-transform:translateY(${1:0});
	-moz-transform:translateY($1);
	-ms-transform:translateY($1);
	-o-transform:translateY($1);
	transform:translateY($1);

	tf:tlz
	-webkit-transform:translateZ(${1:0});
	-moz-transform:translateZ($1);
	-ms-transform:translateZ($1);
	-o-transform:translateZ($1);
	transform:translateZ($1);

	tf:tl3
	-webkit-transform:translate3d(${1:0});
	-moz-transform:translate3d($1);
	-ms-transform:translate3d($1);
	-o-transform:translate3d($1);
	transform:translate3d($1);

	tfo
	-webkit-transform-origin:${1:0} ${2:0};
	-moz-transform-origin:$1 $2;
	-ms-transform-origin:$1 $2;
	-o-transform-origin:$1 $2;
	transform-origin:$1 $2;

	an
	-webkit-animation:$1;
	-moz-animation:$1;
	-ms-animation:$1;
	-o-animation:$1;
	animation:$1;

	an+
	-webkit-animation:${1:name} ${2:1s} ${3:infinite};
	-moz-animation:$1 $2 $3;
	-ms-animation:$1 $2 $3;
	-o-animation:$1 $2 $3;
	animation:$1 $2 $3;

	an:n
	-webkit-animation:none;
	-moz-animation:none;
	-ms-animation:none;
	-o-animation:none;
	animation:none;

	ann
	-webkit-animation-name:$1;
	-moz-animation-name:$1;
	-ms-animation-name:$1;
	-o-animation-name:$1;
	animation-name:$1;

	ann:n
	-webkit-animation-name:none;
	-moz-animation-name:none;
	-ms-animation-name:none;
	-o-animation-name:none;
	animation-name:none;

	andu
	-webkit-animation-duration:${1:1s};
	-moz-animation-duration:$1;
	-ms-animation-duration:$1;
	-o-animation-duration:$1;
	animation-duration:$1;

	anps
	-webkit-animation-play-state:$1;
	-moz-animation-play-state:$1;
	-ms-animation-play-state:$1;
	-o-animation-play-state:$1;
	animation-play-state:$1;

	anps:r
	-webkit-animation-play-state:running;
	-moz-animation-play-state:running;
	-ms-animation-play-state:running;
	-o-animation-play-state:running;
	animation-play-state:running;

	anps:p
	-webkit-animation-play-state:paused;
	-moz-animation-play-state:paused;
	-ms-animation-play-state:paused;
	-o-animation-play-state:paused;
	animation-play-state:paused;

	antf
	-webkit-animation-timing-function:$1;
	-moz-animation-timing-function:$1;
	-ms-animation-timing-function:$1;
	-o-animation-timing-function:$1;
	animation-timing-function:$1;

	antf:e
	-webkit-animation-timing-function:ease;
	-moz-animation-timing-function:ease;
	-ms-animation-timing-function:ease;
	-o-animation-timing-function:ease;
	animation-timing-function:ease;

	antf:l
	-webkit-animation-timing-function:linear;
	-moz-animation-timing-function:linear;
	-ms-animation-timing-function:linear;
	-o-animation-timing-function:linear;
	animation-timing-function:linear;

	antf:ei
	-webkit-animation-timing-function:ease-in;
	-moz-animation-timing-function:ease-in;
	-ms-animation-timing-function:ease-in;
	-o-animation-timing-function:ease-in;
	animation-timing-function:ease-in;

	antf:eo
	-webkit-animation-timing-function:ease-out;
	-moz-animation-timing-function:ease-out;
	-ms-animation-timing-function:ease-out;
	-o-animation-timing-function:ease-out;
	animation-timing-function:ease-out;

	antf:eio
	-webkit-animation-timing-function:ease-in-out;
	-moz-animation-timing-function:ease-in-out;
	-ms-animation-timing-function:ease-in-out;
	-o-animation-timing-function:ease-in-out;
	animation-timing-function:ease-in-out;

	antf:cb
	-webkit-animation-timing-function:cubic-bezier(${1:0}, ${2:0}, ${3:0}, ${4:0});
	-moz-animation-timing-function:cubic-bezier($1, $2, $3, $4);
	-ms-animation-timing-function:cubic-bezier($1, $2, $3, $4);
	-o-animation-timing-function:cubic-bezier($1, $2, $3, $4);
	animation-timing-function:cubic-bezier($1, $2, $3, $4);

	antf:ss
	-webkit-animation-timing-function:step-start;
	-moz-animation-timing-function:step-start;
	-ms-animation-timing-function:step-start;
	-o-animation-timing-function:step-start;
	animation-timing-function:step-start;

	antf:se
	-webkit-animation-timing-function:step-end;
	-moz-animation-timing-function:step-end;
	-ms-animation-timing-function:step-end;
	-o-animation-timing-function:step-end;
	animation-timing-function:step-end;

	antf:s
	-webkit-animation-timing-function:steps($1);
	-moz-animation-timing-function:steps($1);
	-ms-animation-timing-function:steps($1);
	-o-animation-timing-function:steps($1);
	animation-timing-function:steps($1);

	ande
	-webkit-animation-delay:${1:1s};
	-moz-animation-delay:$1;
	-ms-animation-delay:$1;
	-o-animation-delay:$1;
	animation-delay:$1;

	anic
	-webkit-animation-iteration-count:$1;
	-moz-animation-iteration-count:$1;
	-ms-animation-iteration-count:$1;
	-o-animation-iteration-count:$1;
	animation-iteration-count:$1;

	anic:i
	-webkit-animation-iteration-count:infinite;
	-moz-animation-iteration-count:infinite;
	-ms-animation-iteration-count:infinite;
	-o-animation-iteration-count:infinite;
	animation-iteration-count:infinite;

	andi
	-webkit-animation-direction:$1;
	-moz-animation-direction:$1;
	-ms-animation-direction:$1;
	-o-animation-direction:$1;
	animation-direction:$1;

	andi:n
	-webkit-animation-direction:normal;
	-moz-animation-direction:normal;
	-ms-animation-direction:normal;
	-o-animation-direction:normal;
	animation-direction:normal;

	andi:a
	-webkit-animation-direction:alternate;
	-moz-animation-direction:alternate;
	-ms-animation-direction:alternate;
	-o-animation-direction:alternate;
	animation-direction:alternate;

## Layout

	ub
	unicode-bidi:$1;

	ub:n
	unicode-bidi:normal;

	ub:e
	unicode-bidi:embed;

	ub:bo
	unicode-bidi:bidi-override;

	dir
	direction:$1;

	dir:l
	direction:ltr;

	dir:r
	direction:rtl;

	col
	-webkit-columns:${1:0} ${2:0};
	-moz-columns:$1 $2;
	columns:$1 $2;

	cos
	-webkit-column-span:$1;
	-moz-column-span:$1;
	column-span:$1;

	cos:n
	-webkit-column-span:none;
	-moz-column-span:none;
	column-span:none;

	cos:a
	-webkit-column-span:all;
	-moz-column-span:all;
	column-span:all;

	cow
	-webkit-column-width:${1:100px};
	-moz-column-width:$1;
	column-width:$1;

	cow:a
	-webkit-column-width:auto;
	-moz-column-width:auto;
	column-width:auto;

	coc
	-webkit-column-count:$1;
	-moz-column-count:$1;
	column-count:$1;

	coc:a
	-webkit-column-count:auto;
	-moz-column-count:auto;
	column-count:auto;

	cof
	-webkit-column-fill:$1;
	-moz-column-fill:$1;
	column-fill:$1;

	cof:a
	-webkit-column-fill:auto;
	-moz-column-fill:auto;
	column-fill:auto;

	cof:b
	-webkit-column-fill:balance;
	-moz-column-fill:balance;
	column-fill:balance;

	cog
	-webkit-column-gap:$1;
	-moz-column-gap:$1;
	column-gap:$1;

	cog:n
	-webkit-column-gap:normal;
	-moz-column-gap:normal;
	column-gap:normal;

	cor
	-webkit-column-rule:$1;
	-moz-column-rule:$1;
	column-rule:$1;

	cor:n
	-webkit-column-rule:none;
	-moz-column-rule:none;
	column-rule:none;

	cor+
	-webkit-column-rule:${1:1px} ${2:solid} ${3:#000};
	-moz-column-rule:$1 $2 $3;
	column-rule:$1 $2 $3;

	corc
	-webkit-column-rule-color:${1:#000};
	-moz-column-rule-color:$1;
	column-rule-color:$1;

	cors
	-webkit-column-rule-style:${1:solid};
	-moz-column-rule-style:$1;
	column-rule-style:$1;

	cors:n
	-webkit-column-rule-style:none;
	-moz-column-rule-style:none;
	column-rule-style:none;

	corw
	-webkit-column-rule-width:${1:1px};
	-moz-column-rule-width:$1;
	column-rule-width:$1;

	brb
	break-before:$1;

	brb:a
	break-before:auto;

	brb:al
	break-before:always;

	brb:av
	break-before:avoid;

	brb:l
	break-before:left;

	brb:r
	break-before:right;

	brb:p
	break-before:page;

	brb:c
	break-before:column;

	brb:ap
	break-before:avoid-page;

	brb:ac
	break-before:avoid-column;

	bri
	break-inside:$1;

	bri:a
	break-inside:auto;

	bri:av
	break-inside:avoid;

	bri:ap
	break-inside:avoid-page;

	bri:ac
	break-inside:avoid-column;

	bra
	break-after:$1;

	bra:a
	break-after:auto;

	bra:al
	break-after:always;

	bra:av
	break-after:avoid;

	bra:l
	break-after:left;

	bra:r
	break-after:right;

	bra:p
	break-after:page;

	bra:c
	break-after:column;

	bra:ap
	break-after:avoid-page;

	bra:ac
	break-after:avoid-column;

	pbb
	page-break-before:$1;

	pbb:a
	page-break-before:auto;

	pbb:al
	page-break-before:always;

	pbb:l
	page-break-before:left;

	pbb:r
	page-break-before:right;

	pbi
	page-break-inside:$1;

	pbi:a
	page-break-inside:auto;

	pbi:av
	page-break-inside:avoid;

	pba
	page-break-after:$1;

	pba:a
	page-break-after:auto;

	pba:al
	page-break-after:always;

	pba:l
	page-break-after:left;

	pba:r
	page-break-after:right;

	orp
	orphans:$1;

	wid
	widows:$1;

## Document

	zo
	zoom:$1;

	mszo
	-ms-zoom:$1;

	zo:a
	zoom:auto;

	maz
	max-zoom:$1;

	maz:a
	max-zoom:auto;

	miz
	min-zoom:$1;

	miz:a
	min-zoom:auto;

	uz
	user-zoom:$1;

	uz:z
	user-zoom:zoom;

	uz:f
	user-zoom:fixed;

	or
	orientation:$1;

	or:a
	orientation:auto;

	or:p
	orientation:portrait;

	or:l
	orientation:landscape;

## Special

	e
	expression($1)