# NIRS_sample_data
Sample fNIRS data from block-design finger tapping experiment. Acquisition performed using NIRScout (NIRx) system with data acquisition software NIRStar version 15.3.
MNE support for data acquired with NIRStar currently limited to versions 15.0 and 15.2.

The finger tapping experiment consists of 5 blocks, each 25 seconds of finger-tapping followed by 25 seconds of rest. The montage consists of 8 sources and 4 detectors covering bilateral motor regions.

Dataset contains raw data files as well as data preprocessed using nirsLAB (event markers, bandpass filtering, computation of hemodynamic states, etc.).
The ***exportData*** directory contains figures displaying block events (*motor_events.png*), probe montage (*motor_probes_montage.png* for 3D view and *motor_probes_montage_topo.png* for 2D view) and block averages for (de)oxyhemoglobin time-courses (*motor_block_averages.png*).

The following command serves to import data using MNE-Python:

**raw_intensity = mne.io.read_raw_nirx("full_path_to_data/NIRS_sample_data")**

However, this results in the following error message:

**RuntimeError: MNE does not support this NIRStar version ("15.3")**
