# johnadamsbab

import pandas as pd

# Replace these placeholders with your actual accuracy values
data = {
    'Experiment': ['Base Model', 'Batch 64 Model', 'Epoch 200 Model', '3 Hidden Layers Model'],
    'Train Accuracy': ['[Base Train]', '[Batch 64 Train]', '[Epoch 200 Train]', '[3 Hidden Train]'],
    'Validation Accuracy': ['[Base Validation]', '[Batch 64 Validation]', '[Epoch 200 Validation]', '[3 Hidden Validation]'],
    'Test Accuracy': ['[Base Test]', '[Batch 64 Test]', '[Epoch 200 Test]', '[3 Hidden Test]'],
}

df = pd.DataFrame(data)
df
