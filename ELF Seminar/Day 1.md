## Một số command trên linux cần biết:
- cp (copy files and directories)
    * Copy file :               cp file1.txt /path/to/destination/
    * Copy and rename:          cp file1.txt file2.txt
    * Copy directory:           cp -r folder1/ /path/to/destination/
- mv (move (rename) files)
    * Move file:                mv file1.txt /path/to/destination/
    * Move directory:           mv folder1/ /path/to/destination/
    * Cut and rename:           mv oldname.txt newname.txt
- rm (remove files or directories)
    * rm không có thùng rác – xóa là mất!
    * Remove file:              rm file1.txt
    * Remove directory:         rm -r folder1/
- file (determine file type)
    * file hello.cpp:   hello.cpp: C source, ASCII text
    * file hello.o:     hello.o: ELF 64-bit LSB relocatable, x86-64, version 1 (SYSV), not stripped
    * file hello:       hello: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=7bfdbf62ba210e1e016b9d4dcdc83014d8aa3183, for GNU/Linux 3.2.0, not stripped

- xxd (make a hex dump or do the reverse)
    * hình như chỉ dùng được vs file ELF 
    * xxd -l 16 hello:  00000000: 7f45 4c46 0201 0100 0000 0000 0000 0000  .ELF............
- strip (discard symbols and other data from object files)
    * Lệnh strip trong Linux dùng để loại bỏ các thông tin không cần thiết (debug symbols, symbol tables, relocation info...) khỏi file object hoặc executable, giúp giảm kích thước file và ẩn thông tin nội bộ.
    * before strip: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=7bfdbf62ba210e1e016b9d4dcdc83014d8aa3183, for GNU/Linux 3.2.0, not stripped
        ** 16344 bytes
    * after strip:  ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=7bfdbf62ba210e1e016b9d4dcdc83014d8aa3183, for GNU/Linux 3.2.0, stripped
        ** 14472 bytes
- objdump (display information from object files)
    * objdump -t hello | less

- nm (list symbols from object files)
- ldd (print shared object dependencies)
- readelf (display information about ELF files)
- vim (Vi IMproved, a programmer's text editor)
- g++/gcc (launch a C/C++ application)
    * Build ra file .0 - ELF 64-bit LSB relocatable: 
        g++ -c hello.cpp -o hello.o
    * Build ra file ELF - ELF 64-bit LSB pie executable
        g++ hello.cpp -o hello
- java (launch a Java application)
- docker (Docker image and container command line interface)

# Magic number 
- 

## ELF 
- Relocatable file VS Executable file VS Shared library 
- ELF organization 
- ELF header 
- Dynamic linking 
- Lazy binding 
- 