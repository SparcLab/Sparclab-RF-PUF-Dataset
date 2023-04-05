# Sparclab-RF-PUF-Dataset
A dataset containing 30 Xbee S2C transmitter data for both including and excluding wireless channel

## Download Link
* ### **Box**: [Sparclab RF-PUF Dataset Download Link 2](https://purdue.box.com/v/sparclab-rf-puf-dataset)
### ___Note: To download from **BOX**, you will need permission from Dr. Sen first. Just send an email at shreyas@purdue.edu. Once he grants access, you can download directly from the link above.___
### ___For any issue regarding this dataset, download links, or any feedback, send an email to Md Faizul Bari at mbari@purdue.edu___

## Cite This Dataset
If you use this dataset, please cite [this paper](https://www.frontiersin.org/articles/10.3389/felec.2022.856284/full) : 

**M. F. Bari, P. Agrawal, B. Chatterjee, and S. Sen, “Statistical Analysis Based Feature Selection Enhanced RF-PUF With >99.8% Accuracy on Unmodified Commodity Transmitters for IoT Physical Security,” Frontiers in Electronics, vol. 3, Apr. 2022, doi: https://doi.org/10.3389/felec.2022.856284.**
‌

## Experimental Setup
* **Transmitter**: Xbee S2C module, 30 modules used as 30 transmitters. To know detail about Xbee S2C, check: https://www.digi.com/resources/library/data-sheets/ds_xbee-s2c-802-15-4

![XBEE](https://user-images.githubusercontent.com/72578615/149040002-a0e61e44-7c8d-42cc-97dd-ad27ca134eb7.png)

* ### **Receiver**: 1 Xbee S2C module used as a receiver.
* ### **SDR**: Hack-RF One module used as a software-defined radio that is used to sniff data
* ### **Software**: Raw data are collected and stored using GNURadio in binary format (these are the files provided above as downloadables). These binary files are processed in MATLAB.
* ### **Description**: 
TX and RX are kept 1m apart. A 31-bit pseudo-random bit sequence (PRBS) was generated in MATLAB and fed to each TX which transmitted data for 60 sec with QPSK modulation at 2.465 GHz and 230400 bps baud rate. A Hack-RF SDR was connected either to the TX (case1: HackRF getting data directly from TX, ignoring wireless channel) or RX (case2: HackRF getting received data, hence wireless channel is being considered) using a SMA cable. Data captured on HackRF are sampled at 6 mega sample per second and stored in binary format. 

![setup](https://user-images.githubusercontent.com/72578615/149039733-ab89b788-e0b8-491e-a831-2b7628e9bd46.png)

GNURadio also shows live constellation of collected data at a certain time interval. Since data samples within that interval have different freqeuncy offset, the live constellation looks as if it is rotating (shown in the left inset above). After processing the data in Matlab and correcting for frequency offset and timing error, the constellation looks as it should be in QPSK modulation (shown in the right inset above) 
