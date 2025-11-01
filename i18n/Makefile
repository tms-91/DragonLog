VENV_BIN ?= ../venv/bin
QT6_TOOLS ?= $(VENV_BIN)/qt6-tools lrelease
PYLUPDATE6 ?= $(VENV_BIN)/pylupdate6

NO_OBSOLETE?=

TRANSLATIONS = de en templ
TS_FILES = $(foreach transl,$(TRANSLATIONS),DragonLog_$(transl).ts)
QM_FILES = $(TS_FILES:.ts=.qm)

all: $(QM_FILES)
	mkdir -p ../dragonlog/data/i18n;
	cp *.json ../dragonlog/data/i18n;

%.qm: %.ts
	$(PYLUPDATE6) $(NO_OBSOLETE) ../dragonlog ../ui_files -ts $< ;
	$(QT6_TOOLS) $< -qm $@;
	mkdir -p ../dragonlog/data/i18n;
	cp $@ ../dragonlog/data/i18n;

clean:
	rm -f *.qm
	rm -f ../dragonlog/data/i18n/*.qm
	rm -f ../dragonlog/data/i18n/*.json

.PHONY: $(TS_FILES)
