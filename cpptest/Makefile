# Makefile for echo client and server

CXX=		g++ $(CCFLAGS)
TEST=		main.o
OBJS =		$(TEST)

LIBS=

CCFLAGS= -g

all:	test

test:$(TEST)
	$(CXX) -o test $(TEST) $(LIBS)

clean:
	rm -f $(OBJS) $(OBJS:.o=.d)

realclean:
	rm -f $(OBJS) $(OBJS:.o=.d) test 
	
%.d:	%.cc
	$(SHELL) -ec '$(CC) -M $(CPPFLAGS) $< \
		| sed '\''s/\($*\)\.o[ :]*/\1.o $@ : /g'\'' > $@; \
		[ -s $@ ] || rm -f $@'
	
-include $(OBJS:.o=.d)
