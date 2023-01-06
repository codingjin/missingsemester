CC := clang
CXX := clang++

.PHONY: all
all: answer

objects := main.o answer.o

answer: $(objects)
	$(CXX) -o $@ $^

# make 可以自动推断 .o 目标文件需要依赖同名的.cpp文件
# 所以其实不需要在依赖中指定main.cpp 和 answer.cpp
# 也不需要写编译commands, 它知道要用CXX变量指定的命令 作为C++编译器
#
# 这里只需要指定目标文件所依赖的头文件，使头文件变动时可以重新编译对于目标文件 
#

main.o: answer.hpp
answer.o: answer.hpp


.PHONY: clean
clean:
	rm -f answer *.o
