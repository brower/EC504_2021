.SUFFIXES:
.SUFFIXES: .o .cpp
#============================================================
TARGET	=  power

C_SOURCES =  myPowerEnsemble.cpp
C_OBJS     = myPowerEnsemble.o
MY_INCLUDES = rng.h

CCX = g++
CXXFLAGS = -g -std=c++11  -Wall -Iinclude

#============================================================
all: $(TARGET)

.o:.cpp	$(MY_INCLUDES)
	$(CCX)  -c  $(CXXFLAGS) $<  

$(TARGET) :   $(C_OBJS)
	$(CCX) $(CXXFLAGS)  $^ $(LIBDIRS)  -o $@

# Implicit rules: $@ = target name, $< = first prerequisite name, $^ = name of all prerequisites
#============================================================

ALL_SOURCES =  $(C_SOURCES) $(MY_INCLUDES) makefile

INPUT_FILES  = 

clean:
	rm -f $(TARGET) $(C_OBJS) core *~

tar: $(ALL_SOURCES) $(INPUT_FILES)
	tar cvf $(TARGET).tar $(ALL_SOURCES)  $(INPUT_FILES)

$(TARGET).ps: $(ALL SOURCES) 
	enscript -pcode.ps $(ALL_SOURCES)


