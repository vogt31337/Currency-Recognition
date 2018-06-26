# aponteeduardo@gmail.com
# copyright (C) 2017

# ===========================================================================
# Set up
# ===========================================================================
SUBDIRS = Transformations
SRCDIR = $(abs_top_srcdir)
# Include the source directory and the project wide header
# CXXFLAGS += -I$(SRCDIR) -I$(SRCDIR)/include -std=c++11 -Wall -pedantic
CXXFLAGS += -I$(SRCDIR) -I../ImageAnalysis -std=c++11 -Wall -pedantic

SRC_FILES = $(wildcard *.cpp)
OBJ_FILES = $(patsubst %.cpp,%.o,$(SRC_FILES))

#all : ImagePreprocessor.o ImageAnalysis.o ImageDetector.o
all : $(OBJ_FILES)

# ===========================================================================
# Compilation
# ===========================================================================

# I prefer to always have first compilation and then linking,
# as it tends to be easier to debug.

%.o: %.cpp
	$(CXX) $(CXXFLAGS) $(OPENCV_CFLAGS) -c -o $@ $<

# ===========================================================================
# Link
# ===========================================================================

clean:
	rm *.o
