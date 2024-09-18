CC=g++

TARGET = mkl.exe

CPPFLAGS = -g
LDFLAGS = 

INCLD = -I${MKLROOT}/include
LIB  =  -L${MKLROOT}/lib -lmkl_intel_lp64 -lmkl_sequential -lmkl_core -lpthread -lm -ldl

SOURCES = $(wildcard *.cpp)
HEADERS = $(wildcard *.hpp)
OBJECTS = $(SOURCES:.cpp=.o)

all: $(TARGET)
clean:
	rm -f $(OBJECTS) $(TARGET)
$(TARGET) : $(OBJECTS)
	$(CC) $(CPPFLAGS) $(LDFLAGS) $(OBJECTS) -o $@ $(INCLD) $(LIB)
%.o : %.cpp
	$(CC) $(CPPFLAGS) -c $< -o $@ $(INCLD)
