COMPILER=
ARCHIVER=
CP=cp
COMPILER_FLAGS=
EXTRA_COMPILER_FLAGS= -Wall -Wextra
LIB=libxil.a

RELEASEDIR=../../../lib
INCLUDEDIR=../../../include
INCLUDES=-I./. -I${INCLUDEDIR}

INCLUDEFILES=*.h

LIBSOURCES=*.c
OUTS = *.o
OBJECTS =	$(addsuffix .o, $(basename $(wildcard *.c)))

libs:
	echo "Compiling hdcp22_rng"
	$(COMPILER) $(COMPILER_FLAGS) $(EXTRA_COMPILER_FLAGS) $(INCLUDES) $(LIBSOURCES)
	$(ARCHIVER) -r ${RELEASEDIR}/${LIB} $(OUTS)
	make clean

include:
	 ${CP} ${INCLUDEFILES} ${INCLUDEDIR}

clean:
	rm -rf ${OBJECTS}
