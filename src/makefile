#variables
CFLAGS = -Wall

#target exe
all: proj_refactor_file.o fileio.o utils.o
	g++ $(CFLAGS) -o myexe proj_refactor_file.o fileio.o utils.o 

	
#rebuild object file if fileio.cpp, or fileio.h or constants.h changes
#compile the .cpp file to an object file (-c)
fileio.o: ../fileio/fileio.cpp ../includes/fileio.h ../includes/constants.h
	g++ $(CFLAGS) -c ../fileio/fileio.cpp
	
#rebuild object file if utils.cpp, or utils.h or constants.h changes
#compile the .cpp file to an object file (-c)
utils.o: ../utils/utils.cpp ../includes/utils.h ../includes/constants.h
	g++ $(CFLAGS) -c ../utils/utils.cpp
	

proj_refactor_file.o: proj_refactor_file.cpp	
	g++ $(CFLAGS) -c ../src/proj_refactor_file.cpp

#type 'make clean' to remove following	
clean:
	rm -f *.o myexe