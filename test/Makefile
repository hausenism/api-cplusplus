CFLAGS = -g -Wall -std=c++11 -fPIC -DLINUX -DLOGGING_LEVEL_2 -DLINUX -O0 
INCLUDES= -I../include
OBJS=test.o

all: $(OBJS)
	g++ -L../bin/linux_x64 -L../bin/mingw_x64 -L../bin/vx2017_x64 $(OBJS) $(CFLAGS)  -lDolphinDBAPI -lssl  -lpthread -luuid -L../bin  -Wl,-rpath,.:../bin/linux_x64/  -o test 
test.o: test.cpp
	g++ $(CFLAGS) $(INCLUDES) -c test.cpp -o test.o
clean:
	rm *.o test  core -rf
