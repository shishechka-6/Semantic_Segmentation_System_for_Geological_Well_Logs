Semantic Segmentation System for Geological Well Logs

Geological Well Log Segmentation — DeepLabV3+ (PyTorch)

Система семантической сегментации геологических разрезов скважин на основе DeepLabV3+ (ResNet50).
Модель обучена на 40 геологических классах и использует TTA + постобработку, что помогает снижать артефакты и улучшать качество сегментации.
Достигнутая точность: IoU = 0.948 на закрытой тестовой выборке.

📁 Project Structure
wells_segmentation/
│
├── data/
│   └── test_images/           # input images for inference (empty by default)
│
├── work/
│   └── weights/               # place seg_best.pt here (not included in repo)
│   └── runs/                  # output masks after inference
│
├── src/
│   └── infer_seg.py           # inference script
│
├── requirements.txt
└── README.md

📥 Download Model Weights

Файл весов не включён в репозиторий из-за ограничений GitHub.
Скачайте seg_best.pt по ссылке ниже и поместите в:

work/weights/


🔗 Download weights:
(подставь свою ссылку здесь)

🚀 Running Inference
pip install -r requirements.txt
python src/infer_seg.py


Результирующие маски появятся в:

work/runs/

🧰 Tech Stack

Python, PyTorch

DeepLabV3+ (ResNet50)

segmentation-models-pytorch

NumPy, OpenCV, Pillow

Albumentations

CUDA / GPU inference

Kaggle / Colab
