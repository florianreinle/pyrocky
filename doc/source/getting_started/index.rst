.. _ref_index_getting_started:

===============
Getting started
===============

Install PyRocky
---------------

To install PyRocky, run this command:


.. code:: bash

    python -m pip install ansys-rocky-core

or

.. code:: bash

    conda install conda-forge::ansys-rocky-core

Launch PyRocky
--------------

The best way to experiment with PyRocky is by using `Jupyter Notebook <https://jupyter.org/>`_
or `Visual Studio Code <https://code.visualstudio.com>`_. The following code launches a
headless Rocky session and returns a ``RockyClient`` instance from which you can programmatically
interact with the software:

..  code:: python

    import ansys.rocky.core as pyrocky

    rocky = pyrocky.launch_rocky()

You use the ``close()`` method to close the Rocky session:

..  code:: python

    rocky.close()

If you want to launch the Rocky UI, set ``headless=False``:

..  code:: python

    rocky = pyrocky.launch_rocky(headless=False)

Connect to an existing session
------------------------------

Assume that a Rocky session is started with the ``--pyrocky`` option:

.. code::

   C:\Program Files\Ansys Inc\v242\Rocky\bin\Rocky.exe --pyrocky

When the Rocky session is started in this way, you can connect to it with PyRocky:

.. code:: python

    import ansys.rocky.core as pyrocky

    rocky = pyrocky.connect_to_rocky()

Rocky Installation
------------------

To benefit fully from using PyRocky, you must have a licensed copy of Ansys Rocky
installed. The minimum Rocky version supported by PyRocky is 2024 R2.