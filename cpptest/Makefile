cc = gcc

TARGET = hello

$(TARGET) : hello.o
      $(cc) -o $(TARGET) hello.o
      
hello.o : hello.c
      $(cc) -c hello.o hello.c

clean : 
    rm -rf $(TARGET)
