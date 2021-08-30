## 1.1 节练习

> 查阅你使用的编译器的文档，确定它使用的文件命名约定。编译并运行第 2 页的 main 程序。

### GCC and File Extensions

| Extension | Meaning | 
| --- | --- |
| .h | C header file (not to be compiled or linked). |
| .c | C source code which must be preprocessed. |
| .i | C source code which should not be preprocessed. |
| .ii | C++ source code which should not be preprocessed. |
| .cc, .cp, .cxx, .cpp, .c++, .C | C++ source code which must be preprocessed. |
| .f, .for, .FOR | Fortran source code which should not be preprocessed. |
| .F, .fpp, .FPP | Fortran source code which must be preprocessed (with the traditional preprocessor). |
| .r | Fortran source code which must be preprocessed with a RATFOR preprocessor (not included with GCC). |
| .s | Assembler code. |
| .S | Assembler code which must be preprocessed. |
| other | An object file to be fed straight into linking. Any file name with no recognized suffix is treated this way. |

 * [GCC and File Extensions](http://labor-liber.org/en/gnu-linux/development/index.php?diapo=extensions) 
 * [File Types Created for Visual C++ Projects](https://msdn.microsoft.com/en-us/library/3awe4781.aspx)