###############################################################################

LANG1=eus

BASENAME=matxin-$(LANG1)

TARGETS_COMMON=$(LANG1).morph_gen.bin \
	       $(LANG1).measures_gen.bin \
	       $(LANG1).morph_nolex.bin 

###############################################################################

$(LANG1).morph_gen.bin: $(BASENAME).morph_gen_mur.xml 
	lt-comp rl $< $@

$(LANG1).measures_gen.bin: $(BASENAME).measures_gen.xml 
	lt-comp rl $< $@

$(LANG1).morph_nolex.bin: $(BASENAME).morph_nolex.xml 
	lt-comp rl $< $@


###############################################################################

EXTRA_DIST= matxin-eus.generation_move.dat \
	matxin-eus.intrachunk_order.dat \
	matxin-eus.measures_gen.xml \
	matxin-eus.morph_gen_mur.xml \
	matxin-eus.morph_nolex.xml \
	matxin-eus.morph_preproc.dat \
	matxin-eus.semantic.dat \
	matxin-eus.verb_noun_subcat.dat \
	matxin-eus.verb_subcat.dat

matxin_eusdir=$(prefix)/share/matxin/$(BASENAME)
matxin_eus_srcdir=$(prefix)/share/matxin/$(BASENAME)

pkgconfigdir = $(prefix)/share/pkgconfig
pkgconfig_DATA = $(BASENAME).pc

matxin_eus_DATA=$(TARGETS_COMMON)
