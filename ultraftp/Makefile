JDEST = ../../../../bin/util/ultraftp.jar

SOURCES = $(shell echo *.java)
CLASSES = $(SOURCES:%.java=%.class)
ARCHIVE = ultraftp.jar

all: $(CLASSES) $(ARCHIVE)

$(CLASSES): $(SOURCES)
	javac $(SOURCES)

$(ARCHIVE): $(CLASSES)
	jar cvf $(ARCHIVE) *.class
	ls -l $(ARCHIVE)

clean:
	rm -f *.class *.jar

install: $(ARCHIVE)
	@if [ -f $(JDEST) ]; then mv $(JDEST) $(JDEST).prev; fi
	cp $(ARCHIVE) $(JDEST)
	ls -l $(JDEST)*

