# options pour la compilation
CXXFLAGS = -std=c++14 -Wall -Wextra -g
# options pour l'edition de liens
LDFLAGS =
# fichiers contenant des programmes principaux
MAINSRC = ./MainPog.cpp ./MainTest.cpp
# ne pas toucher au reste
SRC = $(filter-out $(MAINSRC), $(shell find . -name "*.cpp"))
OBJ = $(SRC:.cpp=.o)
BIN = $(MAINSRC:.cpp=.out)
.PHONY: all clean
.SECONDARY:
all: $(BIN)
%.out: %.o $(OBJ)
	$(CXX) $(CXXFLAGS) -o $@ $(LDFLAGS) $^
%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $<
clean:
	rm *.o *.out
