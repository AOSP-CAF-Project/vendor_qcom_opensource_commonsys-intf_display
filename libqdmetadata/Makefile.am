h_sources = qdMetaData.h

cpp_sources = qdMetaData.cpp

ifeq ($(TARGET_USES_GRALLOC4),true)
    AM_CPPFLAGS += -DTARGET_USES_GRALLOC4
endif

qdMetaData_includedir = $(pkgincludedir)/display
qdMetaData_include_HEADERS = $(h_sources)

lib_LTLIBRARIES = libqdMetaData.la
libqdMetaData_la_CC = @CC@
libqdMetaData_la_SOURCES = $(cpp_sources)
libqdMetaData_la_CFLAGS = $(AM_CFLAGS) -DLOG_TAG=\"DisplayMetaData\"
libqdMetaData_la_CPPFLAGS = $(AM_CPPFLAGS)
libqdMetaData_LDADD = -lcutils -llog
libqdMetaData_la_LDFLAGS = -shared -avoid-version
