-include ../tools.mk

all:
	$(RUSTC) fakealloc.rs
	$(RUSTC) --edition=2018 --crate-type=rlib ../../../../library/alloc/src/lib.rs --cfg feature=\"external_crate\" --extern external=$(TMPDIR)/$(shell $(RUSTC) --print file-names fakealloc.rs)
