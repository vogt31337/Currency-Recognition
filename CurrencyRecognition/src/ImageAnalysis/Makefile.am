# ===========================================================================
# Set up
# ===========================================================================
SRCDIR = $(abs_top_srcdir)
# Include the source directory and the project wide header
CXXFLAGS += -I$(SRCDIR) -I../ImageAnalysis -std=c++11 -Wall -pedantic

SRC_FILES = $(wildcard *.cpp)
OBJ_FILES = $(patsubst %.cpp,%.o,$(SRC_FILES))

all : $(OBJ_FILES)

# ===========================================================================
# Compilation
# ===========================================================================

# The following line just compiles all files in the folder

%.o: %.cpp
	$(CXX) $(CXXFLAGS) $(OPENCV_CFLAGS) -c -o $@ $<

# ===========================================================================
# Clean
# ===========================================================================

clean:
	rm *.o
