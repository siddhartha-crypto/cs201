TARGET = standard
SOURCES = $(wildcard *.cpp)
HEADERS = $(wildcard *.h*)
OBJECTS = $(SOURCES:%.cpp=%.o)
LD = g++
CXX = g++
CXXFLAGS = -std=c++14 -g -Wall -Iinclude -DGL_SILENCE_DEPRECATION
LDFLAGS = -lfltk

.PHONY: all clean

all: $(TARGET)

clean:
	$(RM) *.o
	$(RM) $(TARGET)

$(TARGET): $(OBJECTS)
	$(LD) -o $@ $(OBJECTS) $(LDFLAGS)

%.o: %.cpp $(HEADERS)
	$(CXX) $(CXXFLAGS) -c $< -o $@

