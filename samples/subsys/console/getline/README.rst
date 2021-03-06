.. _console_getline_sample:

console_getline() Sample Application
####################################

Overview
********

This example shows how to use :cpp:func:`console_getline()` function.
Similar to the well-known ANSI C gets() and fgets() functions,
:cpp:func:`console_getline()` either returns the next available input
line or blocks waiting for one. Using this function, it should be fairly
easy to port existing ANSI C, POSIX, or Linux applications which process
console input line by line. The sample also allows to see details of how
a line is returned by the function.

If you are interested in character by character console input, see
:ref:`console_getchar_sample`.


Requirements
************

UART console is required to run this simple.


Building and Running
********************

The easiest way to run this sample is using QEMU:

.. code-block:: console

   $ cd samples/console/getline
   $ make BOARD=qemu_x86
   $ make BOARD=qemu_x86 run

Now start pressing keys on a keyboard, followed by Enter. The input line
will be printed back, with a hex code of the last character, to show that
line does not include any special "end of line" characters (like LF, CR,
etc.)
