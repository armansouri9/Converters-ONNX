# Converters-ONNX-Version

This repository provides code for converting ONNX models to different versions using Python.

## Installation

To install the required dependencies, run the following commands:

```bash
!pip install onnx
!pip install onnx2torch
```

## Usage

```python
import onnx
from onnx import version_converter
import torch
from onnx2torch import convert

# Load the ONNX model.
model = onnx.load('/content/dr_xxx.onnx')

# Convert the model to the target version.
target_version = 14
converted_model = version_converter.convert_version(model, target_version)

# Convert to torch.
torch_model1 = convert(converted_model)

# Save the converted torch model.
torch.save(torch_model1, '/content/modeldr_xxx.pt')
```

## License


This project is licensed under a Free License.

For more information, please refer to the [repository](https://github.com/armansouri9/Converters-ONNX-Version).
