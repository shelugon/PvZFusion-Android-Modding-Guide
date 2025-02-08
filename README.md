# PvZ Fusion English Android
- **Game APK (2.2.1 Chinese New Year Update)**  
  - [Download the game APK here](https://mega.nz/folder/LUp2Ba7Q#ev_2Q8fdnHsQKQCXDLdq0Q)
- **Chinese global-metadata**
  - [Download the global-metadata here](https://drive.google.com/file/d/192uuShY-98pWI7GfDEcPOMzjIbGQ3tsD/view?usp=sharing)

### 🛠️ Required Tools

- **il2cppdumper**  
- **UABEA**  
- **APK Easy Tool** (or any tool for decompiling, recompiling, and signing APKs)
- **MetaDataStringEditor**
- **Visual Studio Code or NotePad+++**

---

## 📦 How to Use APK Easy Tool

<details>
  <summary><b>APK Easy Tool Instructions</b></summary>

1. **Download APK Easy Tool**:
   - Visit the link [APK Easy Tool on GitHub](https://github.com/mkcs121/APK-Easy-Tool/releases/tag/v1.60) and download the file.

2. **Install APK Easy Tool**:
   - Extract the contents of the `.zip` file to an accessible location, as the folder will be used in the process. Then, run the `APK Easy Tool.exe` file.

3. **Decompile the APK**:
   - Open APK Easy Tool, select the game APK, and click **"Decompile APK"**. This will decompile the APK, allowing access to `data.unity3d`.
   - The APK will be decompiled into the directory "Apk Easy Tool\1-Decompiled APKs" by default.
   [![Tutorial Video](https://img.youtube.com/vi/offl2_-YOPI/maxresdefault.jpg)](https://youtu.be/offl2_-YOPI)
   <sub>(Click the thumbnail to watch the video)</sub>
4. **Recompile the APK**:
   - After making the desired changes to `data.unity3d`, recompile the file using the **"Recompile APK"** option in APK Easy Tool.
   - Select the directory with the decompiled files and click **"Recompile"**.
   - The recompiled APK will be generated in the directory "Apk Easy Tool\2-Recompiled APKs" and will be automatically signed.
   [![Tutorial Video](https://img.youtube.com/vi/HD_pR6I90-s/maxresdefault.jpg)](https://youtu.be/HD_pR6I90-s)
   <sub>(Click the thumbnail to watch the video)</sub>

5. **Install the APK**:
   - After recompiling and signing the APK, you can install it directly on your Android device using the "Install Apk" tool with the device's charging cable connected to the PC for data transfer. 
     (make sure "USB debugging" is enabled on your device).
   - You can also use emulators like **MemuPlay**, **BlueStacks**, or **LDPlayer**.

</details>

---

## 📥 Installing and Opening UABEA

<details>
  <summary><b>UABEA Instructions</b></summary>

1. **Install UABEA**:
   - Visit the official UABEA repository on GitHub:  
     [UABEA GitHub Repository](https://github.com/nesrak1/UABEA)
   - Download the latest version, extract the files to an accessible location, and run the `UABEAvalonia.exe` program.

2. **Open the `data.unity3d` file**:
   - In UABEA, click **File > Open** and select the `data.unity3d` file you want to modify (this file is located in the decompiled APK directory:  
     `Apk Easy Tool\1-Decompiled APKs\DECOMPILED_APK_NAME\assets\bin\Data`).
   - This file contains all compressed data, such as textures, assets, audio, and animations from the game.

3. **Extract the file**:
   - Click **File** to extract the contents and choose a location on your computer to save the extracted `data.unity3d` file. Then, click **Export all** to extract the bundles inside the file, such as `resources.assets`. (Avoid opening the file directly in memory, as this may result in data loss if the application crashes.)

4. **Opening the extracted `data.unity3d` file**:  
   - After extracting `data.unity3d` and its bundles, close UABEA and reopen the program. Then, open the `Extracted DataUnity3D` file.  
   - After loading the file, click the selection tab and choose the **`resources.assets`** bundle to continue editing.
   [![Tutorial Video](https://img.youtube.com/vi/1V9Vn4RyL9E/maxresdefault.jpg)](https://youtu.be/1V9Vn4RyL9E)
   <sub>(Click the thumbnail to watch the video)</sub>
</details>

---

## 📂 Managing Files with UABEA

<details>
  <summary><b>Managing Files with UABEA</b></summary>

1. **Focus only on the `resources.assets` bundle** (as it contains all the necessary information for meaningful translations and changes):
   - Navigate to the `resources.assets` bundle and click **Info** to open the file viewer window.

2. **Searching for files by name**
   - Searching for files by name can be tricky, as the search will only work if you use the exact name of the file you're looking for.  
   - Use the direction options to assist in the search, as if the file is at the top and you search at the bottom, UABEA might not find it.

3. **Apply a view filter**:
   - Go to the **View** tab and apply a filter to make file searching easier.  
   - Focus on the following file formats:
     - **TextAsset**: Contains Almanac data and `Plant_Data`.
     - **Texture2D**: Contains game interface textures, plants, etc.
     - **MonoBehaviour**: Contains game interface text and data. Focus only on files like `Text`, `TextMeshPro`, `TextMeshProUGUI`, and `TMP_InputField` as they contain translation information.
     - **Font**: Contains all fonts used in the game.
</details>

---

## 💾 Saving the `data.unity3d` File After Modifications  

<details>
   <summary><b>Saving the `data.unity3d` File After Modifications</b></summary>  

<sub>Saving the `data.unity3d` file might seem complicated at first, but the process is simpler than it appears. Follow the steps below to ensure your modifications are applied correctly:<sub>
1. **Saving `resources.assets`**  
   - After making all desired changes to `resources.assets`, click **File > Save**.  
   - A window will appear with the message:  
     *"File saved. To complete changes, exit this window and File->Save in bundle window."*  
   - Click **Ok** and close the file viewer window.  

2. **Saving in the bundle manager**  
   - Return to the bundle manager window.  
   - Click **File > Save**.  
   - If the screen freezes, wait a few moments until the process completes and the mini window closes automatically.  

3. **Compressing the `data.unity3d` file**  
   - After saving, click **File > Compress**.  
   - An Explorer window will open, where you should select the **original `data.unity3d` file (not extracted)**, located inside the decompiled APK folder where you're making modifications.  
   - Choose the **LZ4** compression format and wait for the process to complete.  

4. **Finalizing**  
   - Once the save is complete, your modified `data.unity3d` file will be ready to use.  
   - Now, simply recompile the APK again using **APK Easy Tool** and test your changes in the game!  
</details>

---

## 📃 Handling MonoBehaviour with Il2CppDumper

<details>
  <summary><b>MonoBehaviour with Il2CppDumper</b></summary>

When the game is compiled with **Il2Cpp**, the **MonoBehaviour** data is compressed and unreadable in the `resources.assets` file. To resolve this, **Il2CppDumper** is required.

1. **How to Use Il2CppDumper**:
   - Download **Il2CppDumper**: [GitHub Il2CppDumper](https://github.com/Perfare/Il2CppDumper)
   - Provide the `libil2cpp.so` and `global-metadata.dat` files to **Il2CppDumper**.  
   - After the dump process, the program will create a folder named `DummyDll` in your directory.

2. **Configuring UABEA with Il2CppDumper**:
   - Copy the `DummyDll` folder to the same location as the extracted files.
   - Rename the folder to **Managed**.
   - Restart UABEA to ensure the "MonoBehaviour" files are read correctly.

  
   ... [![Tutorial Video](https://img.youtube.com/vi/fRzrsaGr4MM/maxresdefault.jpg)](https://youtu.be/fRzrsaGr4MM)  
     <sub>(Click the thumbnail to watch the video)</sub>
</details>

---

## ✏️ Editing Text Content

<details>
  <summary><b>Editing Text Content</b></summary>

1. **How to Export and Import Text Files**:
   - Use the **Export dump** and **Import dump** features in UABEA to modify text files (you can also edit text directly in UABEA using the Edit Data function).
   - The text is located in files like `Text`, `TextMeshPro`, `TextMeshProUGUI`, and `TMP_InputField` as mentioned earlier.

2. **Editing Game Text**:
   - Some game text is located in MonoBehaviours, and to translate it, you'll need to manually check each file (Text, TextMeshPro, TextMeshProUGUI, and TMP_InputField). Since the text is disorganized, this task can be tedious. Additionally, many files will contain only numbers (usually plant sun costs) or be empty, and these can be ignored. Good luck editing! 🚀

3. **Editing Other Game Text**:
   - Textual information, such as Odyssey bonuses, game text, level introductions, etc., is located in the `global-metadata.dat` file. You can edit it using the `MetaDataStringEditor` (available only in Mandarin).
</details>

---

## 🖼️ Changing Textures

<details>
<summary><b>Instructions for Changing Textures</b></summary>

1. **How to Filter**:
  - To make searching for textures easier, filter by "Texture2D". Click **"View"**, then **"Filter"**, and select **"Deselect All"**. Then, check only **"Texture2D"**. This will display only textures.
  
2. **Searching for a Specific Texture**:
  - To quickly find the texture you want to modify, click **"View"**, then **"Search by Name"**. Enter the exact name of the texture you're looking for. Example: `SeedChooser_Background`.
  
3. **Changing Search Direction**:
  - If you don't find the desired texture, try changing the search direction using the **"Up"** and **"Down"** arrows.

4. **Modifying the Texture**:
  - After locating the texture, select it and click **"Plugins"** > **"Edit Texture"** > **"Load"**. Choose the modified texture and then click **"Save"** to save the changes.

<sub>If you'd like, you can download a file containing all the game textures with their respective names [**Click here**](https://drive.google.com/file/d/12CUC7Lty_KELPHn2RGYabdaqpEA3GhY1/view?usp=sharing).</sub>

</details>

---

## 🖇️ Editing Remaining Text Content with MetaDataStringEditor

<details>
  <summary><b>Editing Remaining Text Content with MetaDataStringEditor</b></summary>

  ### 1. How to Use MetaDataStringEditor:
   - Download **MetaDataStringEditor**: [GitHub MetaDataStringEditor](https://github.com/JeremieCHN/MetaDataStringEditor/releases/tag/0.0) <sub><sub>(Available only in Mandarin)</sub></sub>
   - Download the `global-metadata` located at the top of this tutorial, or use the `global-metadata` located in the folder:
     ```
     Apk Easy Tool\1-Decompiled APKs\DECOMPILED_APK_NAME\assets\bin\Data\Managed\Metadata
     ```
     But **make a backup** before editing.
   
   - The MetaDataStringEditor interface is in Mandarin. Here's an image showing the translation of each button (in English):  
     ![English Buttons](https://i.imgur.com/X1gITCi.png)
  
   - **Be very careful** not to click "Close File". If you close it, you **will lose all your progress**.
   
   - The strings start appearing further down in the file.  
     ![This is where the strings are](https://i.imgur.com/AQ1RjXd.png)
  
   - **Warning**: MetaDataStringEditor can only handle Mandarin (Chinese) strings well. After making changes, saving, and reopening the file, you'll see strange text. However, you can still edit them normally if you know what each text represents; Whenever there 
        is a line break command like \n, manually insert a line break.  
     ![Buggy texts](https://i.imgur.com/IAXH0Xk.png)

</details>

<sub><sub>This method can be applied to any game developed with the Unity engine.</sub></sub>

</details>

For any questions or suggestions, please contact me on Discord: **shelvox** 
🙂
