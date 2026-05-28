# Help System Extraction & Modernization

The game references external Windows help and context files from within the game itself. Specifically, players are unable to access or read BGM donor history entries on modern systems. These help files consist of linked pages containing embedded image content.

Modern versions of Windows no longer support these legacy help formats, so the content must be extracted and converted into a more accessible modern format.

The application `MVIEWER2.EXE` is used to read the English compiled help package `METALSTO.MVB`. Inspection of `MVIEWER2.EXE` identifies it as a Microsoft Multimedia Viewer application.

A utility named **HelpDeco V2.1** can decompile the packed `.MVB` archive into more accessible formats. While the exported formats are easier to work with, they are still not ideal for long-term preservation or web publishing. The extracted formats include:

* `.rtf` — Rich Text Format articles
* `.bmp` — Standard bitmap images
* `.shg` — Segmented Hypergraphics with clickable regions

Another utility, **Help Scribble**, can read `.shg` files and export them as flat `.bmp` images. This process removes the embedded clickable mapping regions, but those regions should be straightforward to recreate using HTML image maps.

A custom conversion tool will likely be required to process each `.rtf` document into modern `.html`.

## File Format Notes

* `.rtf` is a basic rich text format and is relatively easy to parse and convert.
* `.bmp` files already contain usable image content and require no additional processing.
* `.shg` files are interactive images that link to articles depending on where the user clicks. Additional tooling or manual recreation will be required to preserve this functionality.

# High-Level Workflow

1. Decompress `METALSTO.MVB` using HelpDeco V2.1 (HELPDECO.EXE /g /i /s 1 METALSTO.MVB) into "step 1" folder
2. Convert extracted `.shg` files into non-interactive `.bmp` images using Help Scribble into "step 2" folder
3. Manualy created `.html` documents will be needed to made to hold the mapped `.bmp` images into "step 3".
4. Convert extracted `.rtf` articles into modern `.html` using a custom conversion tool
5. Recreate clickable regions using HTML `<map>` areas and associated image content
6. Create parent `.html` pages that integrate the converted text and images
7. Publish the resulting documentation in a modern, accessible format


