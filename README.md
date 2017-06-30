# [CS4065] MMSR: iCompress - Image & Video frame compression based on eye tracking data
iCompress is a compression algorithm suitable for image compression based on eye tracking data. <br />
iCompress makes use of eye fixation data on individual images and video frames and constructs fixation density maps (FDMs) to segment video frames to determine the regions suitable for further compression relative to other regions. <br />
The algorithm splits each image into macro-blocks and uses a simple JPEG encoding scheme with a weighted modified quantization table (based on the standard JPEG quantization table) on each macro-blocks with respect to the regions determined from the FDM. <br />
The quantized Discrete Cosine Transform Coëfficients (DCTCs) then are encoded further in the entropy encoding process. The DCTCs are first ordered in a zig-zag pattern and encoded with Run-Length-Encoding. Finally, the RLE encoded DCTCs are encoded with Canonical Huffman code and saved to its own <code>.icy</code> format.

### Running Jupyter Notebook
To run our Jupyter Notebook (`.ipynb`), we require to first run Jupyter Notebook as a web app on our localhost. <br />
We run in a terminal: <br />
`jupyter notebook` <br />

Open a browser and go to [localhost](http://localhost:8888/). <br />
In case there is no `.ipynb` to be found, use the `upload` button and select the appropriate `.ipynb` accordingly.

### Downloading the video data
Due to the nature of the very large size of the unencoded <code>.yuv</code> Ultra-HD videos [1], they must be [downloaded](http://ivc.univ-nantes.fr/en/databases/HD_UHD_Eyetracking_Videos/) separately. <br />

The notebook only uses the one video of the dataset which can be downloaded separately from [here](https://drive.google.com/uc?id=0B6PBl7t3GGXrUVVzTmhqQURMdGM&export=download).

### References
[1] T. Vigier, J. Rousseau, M. Perreira Da Silva, and P. Le Callet, “A new HD and UHD video eye tracking dataset.” In 7th ACM Multimedia Systems Conference (MMSys), May 2016.