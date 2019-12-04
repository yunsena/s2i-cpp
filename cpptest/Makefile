# Makefile for echo client and server

CXX=			g++ $(CXXFLAGS)

TEST=		main.o
LIB=		lib.o
OBJS =			$(TEST)$(LIB)

LIBS=

CXXFLAGS= -g

all:	test lib

test:$(TEST)
	$(CXX) -o test $(TEST) $(LIBS)
lib:$(LIB)
	$(CXX) -o lib $(LIB) $(LIBS)

clean:
	rm -f $(OBJS) $(OBJS:.o=.d)

realclean:
	rm -f $(OBJS) $(OBJS:.o=.d) test lib

%.o : %.cc
	$(CXX) -c -o $@ -MD -MP ${CPPFLAGS} ${CXXFLAGS} $<
	
-include $(OBJS:.o=.d)
