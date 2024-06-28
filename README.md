# 3D-CNN: Multi-resolution Short-time Fourier Transform Providing Deep Features for 3D CNN to Classify Rolling Bearing Fault Vibration Signals

When performing CNN classification tasks for 1D signals, the most straightforward solution might be to use a 1D CNN (in fact, in many scenarios, this could be the preferred option). We can also use methods to transform 1D data into 2D data to make it suitable for 2D CNNs. These methods include, but are not limited to, time-frequency techniques such as Short-Time Fourier Transform (STFT) and encoding methods like Gramian Angular Fields.

Now, let's discuss the 2D CNN approach using STFT. The Gabor uncertainty principle tells us that we may never find an optimal window length that balances both time resolution and frequency resolution. This means our STFT-CNN might always lose some important information...

But wait, we might be able to do this: generate a series of 2D data using STFT with different window lengths, thus transforming the 1D data into 3D data, and then use a 3D CNN for classification - Let CNN itself decide the problem of Gabor uncertainty. While this is surely not a computationally economical method, its classification performance surpasses that of 1D CNN and 2D STFT-CNN with fixed window lengths.

This case uses a relatively simple CNN structure to illustrate this process. Six types of bearing fault vibration signals are reconstructed into 3D data containing six different window lengths and fed into this 3D CNN for signal classification. Experiments confirm that achieving completely correct and accurate classification with the 3D CNN is quite common on this dataset, while the 1D CNN and 2D STFT-CNN with a fixed window length make some errors.

In this GITHUB repository, I only provide the code; the data can be found in external files here: https://drive.google.com/file/d/17PVOAs7xomwRKY1KUIlE6ltJRqnXo6K8/view?usp=drive_link. You can run it directly, or construct the 3D data in your preferred way (you might need some tricks to ensure consistent data shapes, or use more padding during tests). Alternatively, you can always build a new 3D CNN directly — as the focus of this work is on the concept of the 3D CNN, not any specific CNN architecture.

Please cite the following information to use this method: Meng Zhang, Multi-resolution Short-time Fourier Transform Providing Deep Features for 3D CNN to Classify Rolling Bearing Fault Vibration Signals, Engineering Research Express, 2024，and I would provide DOI as soon as it becomes available. The code is free to use, so please do not sell it.






