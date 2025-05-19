
# 🔐 **Project: Video Encryption and Decryption System**

## 🧠 **Objective**

The goal of this project is to securely encrypt and decrypt a video by treating its **audio** and **visual** components separately. The video is processed frame by frame, and each color channel of the frames is encrypted using a **deterministic noise-based technique**. The audio is also encrypted using the same noise pattern, ensuring full synchronization and security. The decryption process accurately reverses each step to reconstruct the original video.

---

## 🔐 **Encryption Process**

### 🎞️ Step 1: **Separating Audio and Video**

* The original video is split into its two primary components:

  * **Audio stream** is extracted and saved separately.
  * **Video stream** is retained for further frame-based processing.

---

### 🖼️ Step 2: **Frame Extraction**

* The video is broken down into individual frames.
* Each frame is made up of three distinct color channels:

  * **Red (R)**
  * **Green (G)**
  * **Blue (B)**

---

### 🎨 Step 3: **Channel-Wise Frame Encryption**

* A **single, fixed noise pattern** is generated at the beginning and saved for later use.
* Each frame’s R, G, and B channels are encrypted using this predefined noise.
* This method ensures that the process is repeatable and consistent for both encryption and decryption.

---

### 🧱 Step 4: **Reconstructing Encrypted Frames**

* After encrypting all three channels of a frame, they are merged to recreate the encrypted version of that frame.
* All encrypted frames are then saved sequentially.

---

### 📹 Step 5: **Forming the Encrypted Video**

* The encrypted frames are stitched together to create a complete video file (without sound).

---

### 🔊 Step 6: **Encrypting the Audio**

* The extracted audio signal is also processed using the same noise file.
* This results in an encrypted version of the audio, which is saved separately in a secure format.

---

### 📼 Step 7: **Combining Encrypted Audio and Video**

* The encrypted video and audio are both stored as part of the final encrypted package.
* This keeps both components secure and ready for synchronized decryption later.

---

## 🔓 **Decryption Process**

### 📽️ Step 1: **Loading the Encrypted Video**

* The encrypted video is opened and all its frames are extracted in sequence.

---

### 🎨 Step 2: **Decrypting Frame Channels**

* The original noise pattern used during encryption is reloaded.
* Each frame is split into its R, G, and B components.
* The same noise pattern is applied to reverse the encryption process on each channel.
* This restores each color channel to its original form.

---

### 🧱 Step 3: **Reconstructing Original Frames**

* The decrypted R, G, and B channels are combined to recreate the original frame.
* All restored frames are collected and ordered properly.

---

### 🎞️ Step 4: **Rebuilding the Video**

* The decrypted frames are assembled to form a video file, now restored visually but without audio.

---

### 🔊 Step 5: **Decrypting the Audio**

* The encrypted audio file is loaded.
* Using the same noise used during its encryption, the original audio signal is recovered.
* The result is a clean audio file that matches the original.

---

### 📼 Step 6: **Merging Audio and Video**

* The decrypted video and audio are finally combined into a single output file.
* This produces a fully decrypted video identical in content to the original.

---

## ✅ **Key Features**

* **Frame-Level Security**: Every frame is independently encrypted and decrypted.
* **Channel-Specific Handling**: Each color component is treated individually for better control.
* **Noise-Based Technique**: Encryption is based on a consistent noise pattern to ensure reliable decryption.
* **Independent Audio Security**: The audio is handled separately to avoid quality loss.
* **Compression-Free Processing**: No data loss due to compression—ensures exact recovery.

---
