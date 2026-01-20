# Partial-Facial-Recognition-Model

A robust, deep learning-based framework for identity verification in non-ideal conditions where full facial visibility is compromised. This model is specifically engineered to perform accurate recognition using only partial facial features—such as eyes, forehead, or mouth regions—when obstructions like masks, shadows, hands, or poor lighting obscure parts of the face.

Built with **PyTorch**, the system leverages a specialized neural network architecture trained to extract and compare distinctive features from visible facial segments. The pipeline integrates **RetinaFace** for precise initial face detection, even in challenging scenarios, followed by a feature embedding model that is invariant to occlusions.

## Key Features & Technical Stack

*   **Occlusion-Robust Architecture**: A CNN-based model trained with extensive data augmentation (via **Albumentations**) to generalize across various partial visibility patterns.
*   **Efficient Processing**: Utilizes **FAISS** for fast similarity search and vector matching, enabling quick identification against large registered databases (supports both CPU and GPU backends).
*   **Complete Pipeline**: From detection (`opencv-python`, `retinaface-pytorch`) and preprocessing (`scikit-image`) to feature extraction and matching.
*   **Ready-to-Use Demo**: Includes an interactive **Streamlit** web application for real-time testing, allowing users to upload images/video and see recognition results.
*   **Development Tools**: Comes with training scripts, evaluation metrics, and visualization utilities (`matplotlib`, `tqdm`) for further development and analysis.

## Use Cases
Ideal for security systems with mask mandates, low-light surveillance, applications with user selfie obstructions (e.g., hands holding phones), or any environment requiring reliable identification from incomplete facial data.
