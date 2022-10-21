
>     _________     _____   __________ ___   _______________ 
>     \_   ___ \   /  _  \  \______   \\   \ /   /\_   _____/
>     /    \  \/  /  /_\  \  |       _/ \  \   /  |    __)_  
>     \     \____/    |    \ |    |   \  \    /   |        \ 
>      \______  /\____|__  / |____|_  /   \__/   /_______  / 
>             \/         \/         \/           @HurDFIR\/ 

Carve is a easy way to carve NTFS files such as $MFT and $UsnJrnl attributes from a mounted image. Eventually, this will have a full forensic triage capability. 

## Installation

Carve requires the following Python modules to run. 
* wmi
* pytsk3

The easiest way to install the dependencies is with:
> pip install -r requirements.txt

## How to
> usage: carve.py [-h] --drive DRIVE_LETTER --dest DESTINATION_DIR [--mft | --no-mft] [--usnj | --no-usnj]
                [--full_triage | --no-full_triage]

Arguments | Description
--- | ---
-h, --help | Show help message and exit
--drive | Logical drive to extract from (e.g., "F:")
--dest | Directory to extract files to.
--mft, --no-mft | Optional. Extracts $MFT.
--usnj, --no-usnj | Optional. Extracts NTFS $UsnJrnl:$J, $UsnJrnl:$MAX and $LogFile.
--full_triage, --no-full_triage | Optional. Extracts a full triage of files. Implicitly includes other optional args.

## License

MIT