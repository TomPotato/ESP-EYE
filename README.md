<h1 align="center">The ESP-EYE</h1>

Released in early 2019, the ESP-EYE was a milestone for Espressif's development boards, popular among DIY makers and edge-device developers. A newer board in the same line is the ESP32-S3-EYE, initially developed in late 2021, and so the ESP-EYE has since reached EOL.
<!-- S3-EYE date from first commit in repo, not retail launch -->
But What is it?
ESP-EYE is a development board for image recognition and speech signal processing, on which it integrates an on-board ESP32 chip, a 2 megapixel camera, and a digital microphone, 8MByte PSRAM and 4MByte flash. The board also supports image transmission via Wi-Fi and debugging through a Micro-USB port.

<h3>The Board</h3>
<p float="left">
    <img width="43%" src="./images/readme/ESP-EYE_front.png" alt="front of the ESP-EYE board">
    <img width="56%" src="./images/readme/ESP-EYE_back.png" alt="back of the ESP-EYE board">
</p>
<br clear="all">

<table>
<tr>
<td valign="top" width="50%">
<h3 align="center">Components</h3>
<ul>
<li>
<p dir="auto"><strong>3D_PIFA Antenna</strong></p>
<p dir="auto">A 3D PIFA antenna. With the R14 resistor users can select the external IPEX antenna, whereas with the R15 resistor they can select the 3D antenna.</p>
</li>
<li>
<p dir="auto"><strong>IPEX Connector</strong></p>
<p dir="auto">Used for connecting the external IPEX antenna. With the R14 resistor users can select the external IPEX antenna, whereas with the R15 resistor they can select the 3D antenna.</p>
</li>
<li>
<p dir="auto"><strong>ESP32 Chip</strong></p>
<p dir="auto">A 2.4 GHz Wi-Fi and Bluetooth combo chip.</p>
</li>
<li>
<p dir="auto"><strong>Crystal Oscillator</strong></p>
<p dir="auto">Provides an external clock to ESP32.</p>
</li>
<li>
<p dir="auto"><strong>Flash &amp; PSRAM</strong></p>
<p dir="auto">Provides memory for storing applications.</p>
</li>
<li>
<p dir="auto"><strong>CP2102 USB-to-UART Chip</strong></p>
<p dir="auto">Converts the USB signals to UART signals.</p>
</li>
<li>
<p dir="auto"><strong>USB Port</strong></p>
<p dir="auto">Provides power supply to the whole system.</p>
</li>
<li>
<p dir="auto"><strong>LDO Power Supply</strong></p>
<p dir="auto">Provides the required power supply to the ESP32 chip, camera and LED indicators.</p>
</li>
<li>
<p dir="auto"><strong>Side Tactile Button</strong></p>
<p dir="auto">A function key.</p>
</li>
<li>
<p dir="auto"><strong>Top Tactile Button</strong></p>
<p dir="auto">Reset/Boot button. We recommend that you do not configure this button for other uses.</p>
</li>
<li>
<p dir="auto"><strong>LED Indicators</strong></p>
<p dir="auto">The board has a red and a white indicator. Different flashing combinations of the red and white indicators reflect the different statuses of the board, e.g. waking up, networking, face detection, face recognition, face enrollment and face recognition.</p>
</li>
<li>
<p dir="auto"><strong>Camera</strong></p>
<p dir="auto">An external 2-Megapixel camera module for face detection, face recognition and Face ID enrollment.</p>
</li>
<li>
<p dir="auto"><strong>Camera Connector</strong></p>
<p dir="auto">Used for connecting the external camera.</p>
</li>
<li>
<p dir="auto"><strong>MIC</strong></p>
<p dir="auto">A digital microphone for voice control functions.</p>
</li>
<li>
<p dir="auto"><strong>SPI Port</strong></p>
<p dir="auto">A reserved port for data transmission.</p>
</li>
</ul>
</td>

<td td valign="top" width="50%">
<div align="right" width="50%">
<h3 align="center">Connections</h3>
<table align="center">
<thead>
<tr>
<th align="left">Interface</th>
<th align="center">Camera Pin</th>
<th align="center">ESP-EYE</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SCCB Clock</td>
<td align="center">SIOC</td>
<td align="center">IO23</td>
</tr>
<tr>
<td align="left">SCCB Data</td>
<td align="center">SIOD</td>
<td align="center">IO18</td>
</tr>
<tr>
<td align="left">System Clock</td>
<td align="center">XCLK</td>
<td align="center">IO4</td>
</tr>
<tr>
<td align="left">Vertical Sync</td>
<td align="center">VSYNC</td>
<td align="center">IO5</td>
</tr>
<tr>
<td align="left">Horizontal Reference</td>
<td align="center">HREF</td>
<td align="center">IO27</td>
</tr>
<tr>
<td align="left">Pixel Clock</td>
<td align="center">PCLK</td>
<td align="center">IO25</td>
<td align="center">IO25</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 0</td>
<td align="center">D2</td>
<td align="center">IO34</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 1</td>
<td align="center">D3</td>
<td align="center">IO13</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 2</td>
<td align="center">D4</td>
<td align="center">IO14</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 3</td>
<td align="center">D5</td>
<td align="center">IO35</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 4</td>
<td align="center">D6</td>
<td align="center">IO39</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 5</td>
<td align="center">D7</td>
<td align="center">IO38</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 6</td>
<td align="center">D8</td>
<td align="center">IO37</td>
</tr>
<tr>
<td align="left">Pixel Data Bit 7</td>
<td align="center">D9</td>
<td align="center">IO36</td>
</tr>
<tr>
<td align="left">Camera Reset</td>
<td align="center">RESET</td>
<td align="center">-1</td>
</tr>
<tr>
<td align="left">Camera Power Down</td>
<td align="center">PWDN</td>
<td align="center">-1</td>
</tr>
<tr>
<td align="left">Power Supply 3.3V</td>
<td align="center">3V3</td>
<td align="center">3v3</td>
</tr>
<tr>
<td align="left">Ground</td>
<td align="center">GND</td>
<td align="center">GND</td>
</tr>
</tbody>
</table>
</td>
</tr>
</table>

<br clear="all">

<h3>Some "left behind" data</h3>
The ESP-EYE has a limited quantity of memory to be utilized for the model or for the projects that you may decide to use it for: Flash/PSRAM for model: under ~250KB int8 (leaves headroom for camera buffers, TFLite Micro runtime,eventual Arduino sketch) and takes as inputs a 96×96 grayscale that keeps compute down (grayscale is fine if you're classifying obstacle silhouettes, not needing color)

<h3>How to insert an ML model</h3>
<h5>using TFLite, a custom made model similar to a ResNet and the ESP-IDF</h5>
Requirements: 
To install and use ESP-IDF, you'll need Git, Python 3.0-14.0, and the ESP-IDF Installation Manager (EIM).
Once those are installed, follow the <a href="https://docs.espressif.com/projects/idf-im-ui/en/latest/">Getting Started</a> guide on the Espressif site.
Unfortunately the ESP-EYE, with its limited PSRAM, cannot use a big model like a pretrained ResNet one and needs one modeled to its maximum usage.
So we tailor one that can be uploaded: using the structure of the ResNet model we define this model: ReTINY, with this architecture:


<table align="center">
<thead>
<tr>
<th align="left">Stage</th>
<th align="left">Layers</th>
<th align="center">Output shape</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr>
<th align="cemter">Stem</th>
<th align="center">Conv 3x3</th>
<th align="center">Stride 2</th>
<th align="center">8 filters</th>
</tr>
<tr>
<td>Stage 1</td>
<td>1 residual block, 8→8 channels</td>
<td align="center">48×48×8</td>
<td>Conv 3×3 → Conv 3×3 + skip</td>
</tr>
<tr>
<td>Downsample</td>
<td>Conv 3×3, stride 2, 8→16</td>
<td align="center">24×24×16</td>
<td></td>
</tr>
<tr>
<td>Stage 2</td>
<td>1 residual block, 16→16 channels</td>
<td align="center">24×24×16</td>
<td>Conv 3×3 → Conv 3×3 + skip</td>
</tr>
<tr>
<td>Downsample</td>
<td>Conv 3×3, stride 2, 16→32</td>
<td align="center">12×12×32</td>
<td></td>
</tr>
<tr>
<td>Stage 3</td>
<td>1 residual block, 32→32 channels</td>
<td align="center">12×12×32</td>
<td>Conv 3×3 → Conv 3×3 + skip</td>
</tr>
<tr>
<td>Head</td>
<td>Global average pool → Dense(32→4)</td>
<td align="center">4</td>
<td>Softmax over clear/left/center/right</td>
</tr>
</tbody>
</table>
<br clear="all">

To create a new model you have to change the parameters that are described in the ESP-EYE-Model.py file.
To train your model you will need to create a "data" with internal folders organized per class (every folder has to have its class name) and execute the file with the correct informations.

<table align="center">
<thead>
<tr>
<th align="left">Argument</th>
<th align="center">Type</th>
<th align="center">Default</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>--data_dir</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Path to <code>data/</code> containing <code>train/</code> and <code>val/</code></td>
</tr>
<tr>
<td><code>--epochs</code></td>
<td align="center">int</td>
<td align="center">40</td>
<td>Number of training epochs</td>
</tr>
<tr>
<td><code>--batch_size</code></td>
<td align="center">int</td>
<td align="center">32</td>
<td>Number of samples processed per batch</td>
</tr>
<tr>
<td><code>--lr</code></td>
<td align="center">float</td>
<td align="center">1e-3</td>
<td>Learning rate used during training</td>
</tr>
<tr>
<td><code>--out</code></td>
<td align="center">str</td>
<td align="center">tiny_resnet_obstacle.keras</td>
<td>Output path for the saved model</td>
</tr>
</tbody>
</table>

After creating your model you will have to quantize it as it will not be: first and foremost usable by the ESP-EYE and secondly too large to fit inside its PSRAM (as discussed before).
You can execute the file ESP-EYE-Quantizing.py to do so, with the commands:


<table align="center">
<thead>
<tr>
<th align="left">Argument</th>
<th align="center">Type</th>
<th align="center">Default</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>--model</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Path to the trained <code>.keras</code> model</td>
</tr>
<tr>
<td><code>--data_dir</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Path to <code>data/</code>, using <code>train/</code> for calibration</td>
</tr>
<tr>
<td><code>--out_dir</code></td>
<td align="center">str</td>
<td align="center"><code>./esp_model</code></td>
<td>Output directory for the generated ESP model files</td>
</tr>
</tbody>
</table>

And at last, after completing these necessary steps, you will need to upload of the model, that can be done on the Arduino IDE after installing the necessary Libraries, in this case I used: "esp32" board package (provides esp_camera.h for ESP-EYE) and "TensorFlowLite_ESP32" or the newer "Arduino_TensorFlowLite" / tflite-micro Arduino port.

After flashing the ESP-EYE you can connect it to an Arduino mega or UNO to test its results or you can directly use it on your laptop/pc with the test scripts and evaluate it with the evaluation script:

<h3 align="center">esp_eye_capture.py</h3>
<table align="center">
<thead>
<tr>
<th align="left">Argument</th>
<th align="center">Type</th>
<th align="center">Default</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>--port</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Serial port used to connect to the board, e.g. <code>COM3</code> or <code>/dev/ttyUSB0</code></td>
</tr>
<tr>
<td><code>--baud</code></td>
<td align="center">int</td>
<td align="center">921600</td>
<td>Serial communication baud rate; must match <code>SERIAL_BAUD</code> in the firmware</td>
</tr>
<tr>
<td><code>--out_dir</code></td>
<td align="center">str</td>
<td align="center"><code>./data_own</code></td>
<td>Output directory where collected data is saved</td>
</tr>
<tr>
<td><code>--subset</code></td>
<td align="center">str</td>
<td align="center"><code>train</code></td>
<td>Dataset subset to save; options are <code>train</code> or <code>val</code></td>
</tr>
<tr>
<td><code>--interval</code></td>
<td align="center">float</td>
<td align="center">0.3</td>
<td>Time in seconds between saved frames in burst mode</td>
</tr>
<tr>
<td><code>--no_reset</code></td>
<td align="center">flag</td>
<td align="center">False</td>
<td>Prevents the board from being reset when connecting</td>
</tr>
<tr>
<td><code>--boot_wait</code></td>
<td align="center">float</td>
<td align="center">2.5</td>
<td>Time in seconds to wait after opening the serial port</td>
</tr>
</tbody>
</table>

<h3 align="center">models_evaluation.py</h3>
<table align="center">
<thead>
<tr>
<th align="left">Argument</th>
<th align="center">Type</th>
<th align="center">Default</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>--keras</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Path to the trained float model in <code>.keras</code> format</td>
</tr>
<tr>
<td><code>--tflite</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Path to the quantized INT8 model in <code>.tflite</code> format</td>
</tr>
<tr>
<td><code>--eval_dir</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Path to the evaluation dataset folder containing the four class subfolders</td>
</tr>
<tr>
<td><code>--device_ms</code></td>
<td align="center">float</td>
<td align="center">None</td>
<td>Mean inference time measured on the board, in milliseconds (ms)</td>
</tr>
</tbody>
</table>

<h3 align="center">test-py</h3>
<table align="center">
<thead>
<tr>
<th align="left">Argument</th>
<th align="center">Type</th>
<th align="center">Default</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>--model</code></td>
<td align="center">str</td>
<td align="center">Required</td>
<td>Path to the quantized INT8 model in <code>.tflite</code> format</td>
</tr>
<tr>
<td><code>--eval_dir</code></td>
<td align="center">str</td>
<td align="center">None</td>
<td>Path to the evaluation dataset containing class subfolders such as <code>clear/</code> and <code>left_blocked/</code></td>
</tr>
<tr>
<td><code>--image</code></td>
<td align="center">str</td>
<td align="center">None</td>
<td>Path to a single image to classify</td>
</tr>
<tr>
<td><code>--webcam</code></td>
<td align="center">flag</td>
<td align="center">False</td>
<td>Enables real-time classification using a webcam</td>
</tr>
<tr>
<td><code>--camera</code></td>
<td align="center">int</td>
<td align="center">0</td>
<td>Webcam device index used for video capture</td>
</tr>
<tr>
<td><code>--keras</code></td>
<td align="center">str</td>
<td align="center">None</td>
<td>Optional path to a float <code>.keras</code> model for comparison when using <code>--eval_dir</code></td>
</tr>
</tbody>
</table>

I left the data folder with which I trained my ReTina model, you can use your own as long as you modify  class names in the ESP-EYE-Model.py file and your folder follows your class representation.
You don't need to modify the ESP-EYE-Quantizing.py file as it just compresses the file and doesn't interfere with the folder arrangements.

<h5 align="left">Contributors: <i>Agosti Tommaso</i></h5>