ALL: petsc

CFLAGS = -I${ASL_INC}

include ${PETSC_DIR}/lib/petsc/conf/variables
include ${PETSC_DIR}/lib/petsc/conf/rules

bindir = $(prefix)/bin

petsc: petsc.o fg_nl.o fg_dae.o printing.o
	${CLINKER} -o petsc petsc.o fg_nl.o fg_dae.o printing.o $(ASL_LIB) ${PETSC_LIB}

install: petsc
	${CP} petsc ${bindir}
