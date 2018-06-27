# ===========================================================================
# Set up
# ===========================================================================

SRCDIR = . #$(abs_top_srcdir)

# Include the source directory and the project wide header
CXXFLAGS += -I$(SRCDIR) -I../ImageAnalysis -std=c++11 -Wall -pedantic

GUIUTILS_OBJ = $(wildcard ../GUI/*.o)
IMAGE_OBJ = $(wildcard ../ImageAnalysis/*.o)
IMAGE_LIBS_OBJ = $(wildcard ../libs/*.o)
TRANSFORMATIONS_OBJ = $(wildcard ../libs/Transformations/*.o)

all : cli

# ===========================================================================
# Compilation
# ===========================================================================

# I prefer to always have first compilation and then linking,
# as it tends to be easier to debug.
cli.o : CLI.cpp
	$(CXX) $(CXXFLAGS) $(OPENCV_CFLAGS) -c $^ -o $@

ConsoleInput.o : ConsoleInput.cpp
	$(CXX) $(CXXFLAGS) -c $^ -o $@

# ===========================================================================
# Link
# ===========================================================================

cli : cli.o ConsoleInput.o
	$(CXX) $^ -o $@ $(GUIUTILS_OBJ) $(IMAGE_OBJ) $(IMAGE_LIBS_OBJ) $(TRANSFORMATIONS_OBJ)  $(OPENCV_LIBS) $(LDFLAGS)

clean:
	rm *.o
