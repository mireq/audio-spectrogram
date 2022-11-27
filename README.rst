===========================
Audio spectrogram generator
===========================

Requirements
------------

- numpy
- scipy
- ffmpeg binary
- ffprobe binary

Examples
--------

.. code:: bash

   ./spectrogram audio.wav out.png

.. image:: https://raw.github.com/wiki/mireq/audio-spectrogram/simple.png?v2022-11-27

.. code:: bash

   ./spectrogram audio.wav out.png --scale --grid --colorbar

.. image:: https://raw.github.com/wiki/mireq/audio-spectrogram/scale.png?v2022-11-27

.. code:: bash

   ./spectrogram audio.wav out.png --linear --scale --colormap jet

.. image:: https://raw.github.com/wiki/mireq/audio-spectrogram/linear_jet.png?v2022-11-27

.. code:: bash

   ./spectrogram audio.wav out.png --grid --scale --colorbar --colormap nipy_spectral --gain_min -80 --gain_max -20 --step_size 256 --frequency_min 100 --frequency_max 10000

.. image:: https://raw.github.com/wiki/mireq/audio-spectrogram/custom_frequency.png?v2022-11-27
