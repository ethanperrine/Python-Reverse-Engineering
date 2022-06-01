Usually people like to use **pyarmor** to pack their code, then further compile it with **PyInstaller.**
The command for this goes:
# pyarmor pack -e " --onefile" main.py
* You need pyarmor and pyinstaller for this to work!

and it will appear in the dist folder. 

Now onto unpacking and decompiling it on the latest version of python 3.10

* Use pyinstxtractor from https://github.com/extremecoders-re/pyinstxtractor
* Use Pyc2Bytecode from https://github.com/knight0x07/pyc2bytecode

run the command with pyinstxtractor:
python pyinstxtractor.py <filename>
  take a note of everything it shows
  keep the pyinstaller version and version it was compiled with for future reference.
  drag the main entry point out of file for better organization.
converting the pyc to bytecode.
run Pyc2Bytecode in cmd and use this command
  **python pyc2bytecode.py -p <pyc_file_path> -o <output_file_path>**
and you should see the bytecode in a text file. 
