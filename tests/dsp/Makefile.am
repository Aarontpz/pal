LIBS = -lm

if HOST_IS_EPIPHANY
    SIMPLE = notest.c
else
    AM_CPPFLAGS += @CHECK_CFLAGS@
    LIBS += @CHECK_LIBS@
    SIMPLE = simple.c
endif

LDADD = $(top_builddir)/src/libpal.la

check_PROGRAMS = check_p_acorr \
                 check_p_xcorr

check_p_acorr_SOURCES = check_p_acorr.c \
                        acorr_test_data.h

check_p_xcorr_SOURCES = check_p_xcorr.c \
                        xcorr_test_data_1.h \
                        xcorr_test_data_2.h \
                        xcorr_test_data_3.h

TESTS = $(check_PROGRAMS)

# Ubuntu 14.04 has automake-1.11. Need automake-1.12 for nicer test features.
# This will have to do for now.
TESTS_ENVIRONMENT = ../runtest

