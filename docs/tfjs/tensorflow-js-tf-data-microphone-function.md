# Tensorflow.js tf.data .麦克风()功能

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-麦克风-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-microphone-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.data .麦克风()**函数用于产生一个迭代器，该迭代器使用浏览器的本机 FFT 从麦克风音频流创建频域频谱图张量。

**注意:**

*   This code is only valid when the device has a microphone. When this API runs, it will ask for permission to turn on the microphone.
*   This API only works through the browser environment.

**语法:**

```
tf.data.microphone (microphoneConfig)
```

**参数:**该函数接受如下所示的参数:

*   **Microphone configuration:** The microphone configuration object contains the configuration for reading audio data from the microphone. This is an optional parameter.

该对象包含以下指定的配置:

1.  **Sampling rate Hertz:** Its range is between 44100 and 48000.
2.  **fftsize:** It is a numerical value and must be a power of 2 between 2 and 4 and 2 and 14.
3.  **Column truncation length:** is a numerical value.
4.  **NumFrameSperspectrogram:** 是一个数值。
5.  **音轨限制:**是媒体跟踪约束.
6.  **Smoothing time constant:** is a numerical value.
7.  **包括谱图:**为布尔值。
8.  **包括 veform:** 为布尔值。

**返回值:**返回一个微迭代器。

**例 1:** 运行下面的代码后，会请求允许启动麦克风。给予许可后，下面的代码将返回并给出输出。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling the .data.microphone() function
// with its parameters
const mic = await tf.data.microphone({
   fftSize: 1024,
   columnTruncateLength: 32,
   numFramesPerSpectrogram: 10,
   sampleRateHz:43000,
   includeSpectrogram: true,
   includeWaveform: false
});

// Capturing the data recorded by mircophone
const audioData = await mic.capture();
const spectrogramTensor = audioData.spectrogram;

// Printing the data like sampling rate 
// expected and actual
spectrogramTensor.print();
const waveformTensor = audioData.waveform;
waveformTensor.print();

// Stopping the microphone
mic.stop();
```

**输出:**它给出一个误差，因为这里预期的采样率是 43000，但实际记录的值是 48000。

```
An error occured
Mismatch in sampling rate: Expected: 43000; Actual: 48000
```

**例 2:** 运行下面的代码后，会请求允许启动麦克风。给予许可后，下面的代码将返回并给出输出。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing the configurations of 
// reading audio data from microphone
const x = {
   fftSize: 1024,
   columnTruncateLength: 32,
   numFramesPerSpectrogram: 10,
   sampleRateHz:48000,
   includeSpectrogram: true,
   includeWaveform: false
};

// Calling the .data.microphone() function
// with the parameter specified above
const mic = await tf.data.microphone(x);

// Capturing the data recorded by mircophone
const audioData = await mic.capture();
const spectrogramTensor = audioData.spectrogram;

// Creating an iterator that generate frequency-domain
// spectrogram Tensors from the microphone
spectrogramTensor.print();
const waveformTensor = audioData.waveform;

// Stopping the microphone
mic.stop();
```

**输出:**

```
  Tensor
    [[[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[0        ],
      [0        ],
      [0        ],
      ...,
      [0        ],
      [0        ],
      [0        ]],

     [[-Infinity],
      [-Infinity],
      [-Infinity],
      ...,
      [-Infinity],
      [-Infinity],
      [-Infinity]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#data.microphone