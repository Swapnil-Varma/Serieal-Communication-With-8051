## ▶️ How to Run the ASM File in Keil and Simulate it in Proteus

Follow the steps below to compile the Assembly (`.asm`) file in **Keil µVision**, generate the **HEX file**, and run it in the attached **Proteus simulation**.

---

# 🧩 Step 1: Open Keil µVision

1. Install and open **Keil µVision**
2. Click on:

```text
Project → New µVision Project
```

3. Create a new folder for the project
4. Give your project a name

Example:

```text
Serial_Communication_8051
```

---

# ⚙️ Step 2: Select the Microcontroller

After creating the project:

1. A device selection window will appear
2. Search and select your 8051 microcontroller

Example:

```text
AT89C51
```

or

```text
AT89S52
```

3. Click **OK**

---

# 📄 Step 3: Add the ASM File

1. In the left-side Project window:

   * Right-click on **Source Group 1**
   * Click:

```text
Add New Item to Group 'Source Group 1'
```

2. Select:

```text
Assembly File (.s or .asm)
```

3. Give the file name

Example:

```text
serial.asm
```

4. Paste your Assembly code into the file
5. Save the file using:

```text
Ctrl + S
```

---

# 🔨 Step 4: Build the Project

Now compile the program.

Click:

```text
Project → Build Target
```

or press:

```text
F7
```

If there are no errors, the build will complete successfully.

---

# 📦 Step 5: Generate HEX File

To create the HEX file:

1. Go to:

```text
Project → Options for Target
```

2. Open the **Output** tab
3. Tick:

```text
☑ Create HEX File
```

4. Click **OK**

Now rebuild the project again using:

```text
F7
```

---

# 📁 Step 6: Locate the HEX File

After successful compilation:

1. Open your project folder
2. Go inside the:

```text
Objects
```

folder

3. You will find:

```text
Serial_Communication_8051.hex
```

This HEX file will be loaded into Proteus.

---

# 🖥️ Step 7: Open the Proteus Simulation

1. Open the attached Proteus `.pdsprj` file from the repository
2. Double-click on the 8051 microcontroller in the circuit

Example:

```text
AT89C51 / AT89S52
```

---

# 📂 Step 8: Load the HEX File into Proteus

1. In the Program File section:

   * Click the folder icon 📁
2. Browse and select the generated HEX file

Example:

```text
Serial_Communication_8051.hex
```

3. Click **OK**

---

# ▶️ Step 9: Run the Simulation

Click the **Play ▶️** button in Proteus.

The serial communication system will now start working according to the Assembly program.

---

# 📡 Serial Monitoring

If Virtual Terminal is connected in Proteus:

* TX from 8051 → RX of Terminal
* RX from 8051 → TX of Terminal

You will be able to:

* Send serial data
* Receive serial data
* Monitor UART communication in real time

---

# ⚠️ Important Notes

* Ensure the baud rate in code and Virtual Terminal are the same
* Crystal oscillator frequency should match the code configuration

Common value:

```text
11.0592 MHz
```

* Check TX/RX connections properly

---

# ✅ Expected Output

* Successful UART communication
* Real-time serial transmission and reception
* Proper PCB-level simulation in Proteus
