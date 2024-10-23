cd ..

make

build/mjs -e '1 + 2 * 3'

./build/mjs -l 5 -e '2 + 2'

./build/mjs -e 'ffi("double sin(double)")(1.23)'

./build/mjs -e 'ffi("int atoi(char*)")("12") + 40'

gcc test/t01.c mjs.c -o test/t01.out && test/t01.out