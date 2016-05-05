###############################################################################

LANG1=eus

BASENAME=matxin-$(LANG1)

TARGETS_COMMON=$(LANG1).morph_gen.bin \
	       $(LANG1).measures_gen.bin \
	       $(LANG1).semantic.dat \
	       $(LANG1).morph_preproc.dat \
	       $(LANG1).generation_move.dat \
	       $(LANG1).intrachunk_order.dat \
	       $(LANG1).verb_subcat.dat \
	       $(LANG1).verb_noun_subcat.dat \
	       $(LANG1).morph_nolex.bin 

###############################################################################

$(LANG1).morph_gen.bin: $(BASENAME).morph_gen_mur.xml 
	lt-comp rl $< $@

$(LANG1).measures_gen.bin: $(BASENAME).measures_gen.xml 
	lt-comp rl $< $@

$(LANG1).morph_nolex.bin: $(BASENAME).morph_nolex.xml 
	lt-comp rl $< $@

$(LANG1).semantic.dat: $(BASENAME).semantic.dat
	cp $< $@

$(LANG1).verb_subcat.dat: $(BASENAME).verb_subcat.dat
	cp $< $@

$(LANG1).verb_noun_subcat.dat: $(BASENAME).verb_noun_subcat.dat
	cp $< $@

$(LANG1).intrachunk_order.dat: $(BASENAME).intrachunk_order.dat
	cp $< $@

$(LANG1).generation_move.dat: $(BASENAME).generation_move.dat
	cp $< $@

$(LANG1).morph_preproc.dat: $(BASENAME).morph_preproc.dat
	cp $< $@


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
