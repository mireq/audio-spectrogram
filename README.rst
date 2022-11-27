===========================
Audio spectrogram generator
===========================

Requirements
------------

- numpy
- scipy
- matplotlib
- ffmpeg binary
- ffprobe binary

Usage
-----

Run ``./spectrogram input_audio_file out.png``.

Optional arguments
------------------

--start               Start second
--length              Length of audio
--window              Window function
--colormap            Color map (from matplotlib)
--grid                Generate grid
--scale               Generate scale
--colorbar            Generate collor bar
--linear              Linear y scale
--image_width         Generated image width
--image_height        Generated image height
--gain_min            Minimal gain (default -100dB)
--gain_max            Maximal gain (default -30dB)
--frequency_min       Minimal frequency
--frequency_max       Maximal frequency
--step_size           Number of samples per step

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
