# Notes
Important notes related to correctly programing a VEX cortex

## Printing and Terminal
By: Fred Lu
  + Before uploading code to a cortex, close (control-c) the [pros terminal].
  + To receive the [printf] messages on the [pros terminal], upload any project to the cortex from [Atom].
    The upload itself won't work because the pros terminal is open, but it will enable the cortex so that it can send [printf]
    messages through your currently open [pros terminal].
## Serial Communications Configurations
By: Chris Jerrett
+ Use the following configurations with any serial communications software. Ex: Putty or coolterm:
+ Serial Port: May vary; unplugging and replugging the VEXnet device from the computer should allow you to determine the correct port.
+ Baud Rate: 115200
+ Encoding: 28591 - ISO-8859-1 - Western European (ISO) or equivalent
## Compile Time Issues
By: Chris Jerrett
### undefined reference to ... or implicit declaration of function ...: 
  + A function name is spelled incorrectly, or the function was incorrectly declared in a header file. Custom headers must be included in main.h or in the file in which they are used.
### format ... expects argument of type ..., but argument has type ...: 
  + The value provided to a function like printf() or lcdPrint() does not match the expected type inferred from the format string. Some instances of this warning can be safely ignored, but crashes can occur if types double or long long are mixed with other types.
### assignment makes pointer from integer without a cast: 
  + Typically caused when a C pointer has the wrong number of asterisks to dereference it, or when assigning a constant to pointer (instead of *pointer).
  + examples: 
    ```c
    int *t = NULL;
    int i = *(*(t));
    ```

