VENV_BIN ?= ../venv/bin
UI_FILES = $(wildcard *.ui)
PYUI_FILES = $(UI_FILES:.ui=_ui.py)
PYUIC6 ?= $(VENV_BIN)/pyuic6

all:  $(PYUI_FILES)

%_ui.py: %.ui
	$(PYUIC6) -o $@ $<;
	cp $@ ../dragonlog;

clean:
	rm -f *_ui.py
	rm -f ../dragonlog/*_ui.py
