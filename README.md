# johnadamsbab

import pandas as pd

# Replace these placeholders with your actual accuracy values
data = {
    'Experiment': ['Base Model', 'Batch 64 Model', 'Epoch 200 Model', '3 Hidden Layers Model'],
    'Train Accuracy': [94.56, 96.38, 99.82, 95.41],
    'Validation Accuracy': [94.98, 96.14, 97.50, 95.48],
    'Test Accuracy': [94.63, 95.88, 97.72, 95.39],
}

df = pd.DataFrame(data)
df
