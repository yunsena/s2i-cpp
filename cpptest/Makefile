# Makefile for echo client and server

CXX=			g++ $(CXXFLAGS)

TEST=		main.o
OBJS =			$(TEST)

LIBS=

CXXFLAGS= -g

all:	test

test:$(TEST)
	$(CXX) -o test $(TEST) $(LIBS)

clean:
	rm -f $(OBJS) $(OBJS:.o=.d)

realclean:
	rm -f $(OBJS) $(OBJS:.o=.d) test

-include $(OBJS:.o=.d)
