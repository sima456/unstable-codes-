import pySRDF

def unpack_exe(file_name: str, log_file: str = None):
    emu = pySRDF.Emulator(file_name)
    emu.SetBp("isdirty(eip)")
    if log_file:
        emu.Run(log_file)
    else:
        emu.Run()
    emu.Dump(file_name.replace(".exe", "_unpacked.exe"), pySRDF.DUMP_FIXIMPORTTABLE)
    print("File Unpacked Successfully\n\nThe Disassembled Code\n---------------")

if __name__ == "__main__":
    unpack_exe("upx.exe")
