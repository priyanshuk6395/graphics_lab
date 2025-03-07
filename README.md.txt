# README - Installing MinGW Installer & Configuring Code::Blocks for graphics.h

## Installing MinGW (Provided in Repository)

1. Download the MinGW installer provided in this repository.
2. Run the installer and select the necessary components(under Basic Setup):
   - `mingw32-gcc-g++`
3. Choose the installation directory (recommended: `C:\MinGW`).
---

## Configuring Code::Blocks to Use MinGW

1. Open Code::Blocks.
2. Navigate to `Settings` -> `Compiler`.
3. Under `Selected Compiler`, choose `GNU GCC Compiler`.
4. Click `Toolchain Executables` and set the following paths:
    `C:\MinGW\`
5. Click `OK` to apply changes.

---

## Configuring `graphics.h` in Code::Blocks

### Step 1: Copy Required Files
Copy the following files to the specified directories:

- `graphics.h` and `winbgim.h` → `C:\Program Files (x86)\CodeBlocks\MinGW\include`
- `libbgi.a` → `C:\Program Files (x86)\CodeBlocks\MinGW\lib`

### Step 2: Configure Compiler Settings
1. Open Code::Blocks.
2. Navigate to `Settings` -> `Compiler...` -> `Linker Settings`.
3. **In the Left pane:** Click `Add`, then browse and add:
   - `C:\Program Files (x86)\CodeBlocks\MinGW\lib\libbgi.a`
4. **In the Right pane:** Add the following in `Other linker options`:
   ```
   -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32
   ```

### Step 3: Create and Run a Program
1. Create a new `C++` file in Code::Blocks.
2. Write your graphics code and save it with a `.cpp` extension (not `.c`).
3. Build and run the program.

### Step 4: Enjoy!
If everything is set up correctly, your graphics program should run without issues!

---

## Credits
Guide by [Priyanshu](https://github.com/priyanshuk6395).

