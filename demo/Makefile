TARGET = world.out
ORG = hello.o main.o
$(TARGET): $(ORG)
	@echo '$$@ = $@'
	@echo '$$< = $<'
	@echo '$$^ = $^'
	cc -o $@ $^
%.o: %.c
	@echo 'compiling $<...'
	cc -c -o $@ $<
clean:
	rm -f *.o world.out
