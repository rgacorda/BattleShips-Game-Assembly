
# 🛳️ BattleShips Game in Assembly

A two-player battleship game implemented in x86 Assembly using BIOS and DOS interrupts. This project was developed by:

- **Acorda, Ronjay**  
- **Baday, Glenn**  
- **Cruz, Jedaiah**  
- **Foster, Kelvin**  
- **Galutera, Klidge**  
- **Pugyao, Shedd**

---

## 📁 File Structure

- `BattleShips_(ACORDA, BADAY, CRUZ, FOSTER, GALUTERA, PUGYAO).txt` – Main game source code written in Assembly (MASM/TASM syntax)

---

## 🛠️ Requirements

- [MASM](https://archive.org/details/MASM_611) or [TASM](https://winworldpc.com/product/borland-turbo-assembler) (DOS-based assemblers)
- [DOSBox](https://www.dosbox.com/) (for running 16-bit DOS programs on modern OS)

---

## ⚙️ How to Compile & Run

### ✅ 1. Rename File

First, rename the `.txt` file to have an `.asm` extension:

```bash
mv "BattleShips_(ACORDA, BADAY, CRUZ, FOSTER, GALUTERA, PUGYAO).txt" battleships.asm
```

### 🏗️ 2. Assemble and Link (Using MASM)

```bash
masm battleships.asm;
link battleships.obj;
```

This will produce a `BATTLESHIPS.EXE` file.

> Alternatively, to create a `.COM` file:
```bash
masm battleships.asm;
link /TINY battleships.obj;
exe2bin battleships.exe battleships.com
```

### ▶️ 3. Run with DOSBox

1. Open DOSBox
2. Mount the folder containing your `.COM` or `.EXE`:

```bash
mount c /path/to/your/folder
c:
```

3. Run the program:

```bash
battleships
```

---

## 🎮 Gameplay

- Two players take turns placing ships on a 6×6 board.
- Each player targets coordinates to hit the enemy’s ships.
- ASCII headers and text-based UI display game state and results.
- Win screen is displayed once all ships of a player are destroyed.

---

## 📸 Screenshots

> (Add screenshots here if available, e.g. game start, ship placement, win screen)

---

## 📚 Technical Highlights

- BIOS interrupt `10h` for graphics (screen manipulation)
- DOS interrupt `21h` for input/output
- Modular procedures for input validation, ship placement, and drawing
- Implements basic collision detection and direction flipping on edge contact

---

## 💡 Notes

- Ensure your emulator supports 80×25 text mode (standard for DOSBox).
- The code makes use of low-level memory manipulation and may not run on 64-bit OS without an emulator.

---

## 📜 License

Educational use only. Project developed as part of an academic exercise.
