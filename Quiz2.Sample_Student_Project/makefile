CFLAGS=-Wall
all:build myexe docs
build: collegemain.o course.o college.o zip
	g++ -o build collegemain.o course.o college.o
collegemain.o: collegemain.cc
	g++ -c collegemain.cc
course.o: course.h course.cc
	g++ -c course.cc
college.o: college.h college.cc node.h tarray.h
	g++ -c college.cc
clean:
	rm -f *.o main *~ myexe build
	rm -r html latex
myexe: 
	g++ -o myexe collegemain.o course.o college.o
docs:
	doxygen ./college.cc course.cc collegemain.cc
zip:
	zip -r Doxygen.zip ~/cs3560/Doxygen/Quiz2.Sample_Student_Project
