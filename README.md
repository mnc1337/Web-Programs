# Web-Programs

Package of webprograms. There are 6 programs that are used for different tasks. Every program is standalone and consists of one file, which contains HTML (markup), CSS (styles) and JS (logic). Programs will be also named as `tools`.

---

## Programs in package

- **Audio file generator**: a tool that generates sound wave of sine type based on 5 parameters and writes it to `.wav` file, which contains raw, uncompressed audio. `Required parameters`:
    - sample rate (Hz);
    - duration (s);
    - level (dB);
    - two frequency points:
        - initial (Hz);
        - final (Hz).

- **Frequency generator**: a tool that generates sound wave, but after generating sound wave, it reproduces sound in real time. Also you can adjust channels balance (+1 (L) - all output sound plays from the left speaker; 0 (LR) - channels balance (level is equal in both channels (speakers)); +1 (R) - all output sound plays from the right speaker). `Supported wave types`:
    - sine;
    - square;
    - sawtooth;
    - triangle.

- **Notepad**: a tool that is is used for writing some texts and saving them to files. Has a toolbar with the next buttons:
    - "Open": opens a file;
    - "Save as": saves a file to file system;
    - "Save": updates changes in a file if it was saved to file system before;
    - "Auto-save": automatically saves a file with given interval (in seconds);
    - "Clear": clears text from a file, but not from file (if it is saved to file system before);
    - "Theme": changes theme (light / dark).
Also you can see time of last save of file, current time and number of lines, characters and words.

- **Password generator**: a tool that generates passwords based on 3 parameters:
    - length (default range: from `16` to `1048576` chars), should be multiple of hyphens interval (minimal length is equal to double value of hyphens interval);
    - charset (default: `abcdefghijklmnopqrstuvwxyz0123456789`, but it can be changed);
    - hyphens interval (default: `8`, but it can be changed). 
Password copying is supported.

- **Photo viewer**: a tool that helps to view photos. `It displays two parameters`:
    - scale (%) - can be changed;
    - resolution (px). 
Only images extensions are supported (e.g. `png`, `jpg`, `svg`, `ico`, `apng`, `avif`, `webp`, etc.).

## Security

There is a `_security` folder in projects structure. It contains an archive with a nested archive and an `.asc` file - digital signature. **To check archive originality**, you can download archive, extract nested archive (`.7z`) and `.asc` file from it to directory **selected by you** and use there the next command in Bash/WSL console: `gpg --verify webprograms_archive.7z.asc webprograms_archive.7z` - first parameter is a digital signature (`.asc` file), second parameter is an archive.

## License

This project is licensed under the MIT license. See the `LICENSE` file in root directory for details.

---

*2025, author: mnc1337*