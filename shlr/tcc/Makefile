include ../../config-user.mk
include ../../mk/gcc.mk
OFILES=i386-gen.o libtcc.o tccelf.o tccgen.o tccpp.o 

CFLAGS+=-fPIC -g -ggdb
LDFLAGS=-shared -g -ggdb
SOEXT?=dylib
LIBNAME=libr_tcc.${SOEXT}

all: ${LIBNAME} libr_tcc.a

${LIBNAME}: ${OFILES}
	${CC} -o ${LIBNAME} ${LDFLAGS} ${OFILES}

libr_tcc.a: ${OFILES}
	${AR} -r libr_tcc.a ${OFILES}
	${RANLIB} libr_tcc.a

clean:
	rm -f ${LIBNAME} *.o *.a
