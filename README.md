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
