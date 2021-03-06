.. _examples:

Examples and demos
==================

There are ``2`` very basic examples provided with the library.

Parse block of data
^^^^^^^^^^^^^^^^^^^

In this example, block of data is prepared as big string array and sent to processing function in single shot.
Application can then check if GPS signal has been detected as valid and use other data accordingly.

.. literalinclude:: ../../examples/example.c
    :language: c
    :linenos:
    :caption: Minimum example code

Parse received data from interrupt/DMA
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Second example is a typical use case with interrupts on embedded systems.
For each received character, application uses ``ringbuff`` as intermediate buffer.
Data are later processed outside interrupt context.

.. note::
	For the sake of this example, application *implements* interrupts as function call in *while loop*.

.. literalinclude:: ../../examples/example_buff.c
    :language: c
    :linenos:
    :caption: Example of buffer

.. toctree::
	:maxdepth: 2
