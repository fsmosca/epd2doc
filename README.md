# epd2doc
Embeds chess diagrams from epd file into a document.

## Setup

* Install python version 3.7 or later
* Install requirements
  * pip install chess==1.9.3
  * pip install cairosvg==2.5.2
  * pip install python-docx==0.8.11
  
 Copy the whole repository from command line with:  
 
 ```
 git clone https://github.com/fsmosca/epd2doc.git
 ```
 
 You will get the main.py, sample epd `7men_human.epd` and other files.
  
## Command line

```
python main.py --epd-file 7men_human.epd --output-file sevenmen.docx --max-pos 10 --show-fen
```

## Help

```
python main.py --help
```

```
usage: main.py [-h] --epd-file EPD_FILE --output-file OUTPUT_FILE
               [--board-orientation BOARD_ORIENTATION] [--max-pos MAX_POS]
               [--board-image-pixel-size BOARD_IMAGE_PIXEL_SIZE]
               [--doc-image-inch-size DOC_IMAGE_INCH_SIZE] [--header HEADER]
               [--show-fen] [--show-bm] [--show-id] [--randomize-position]
               [-v]

optional arguments:
  -h, --help            show this help message and exit
  --epd-file EPD_FILE   The file name that contains epd or fen positions,
                        (required=True).
  --output-file OUTPUT_FILE
                        The output docx filename, (required=True).
  --board-orientation BOARD_ORIENTATION
                        The diagram board orientation, (required=False,
                        default=side, values=[side, white, black]).
  --max-pos MAX_POS     The maximum number of positions to embed in the doc,
                        (required=False, default=1000, min=1, max=1e6)
  --board-image-pixel-size BOARD_IMAGE_PIXEL_SIZE
                        The size of the board image in pixel, (required=False,
                        default=None). e.g. --board-image-pixel-size 350
  --doc-image-inch-size DOC_IMAGE_INCH_SIZE
                        The size of the board image in inches in the doc,
                        (required=False, default=3.0).
  --header HEADER       The Text that will appear at the top of the document,
                        (required=False, default="Chess Positions").
  --show-fen            A flag to show epd / fen in the doc.
  --show-bm             A flag to show bm in the doc.
  --show-id             A flag to show epd id in the doc.
  --randomize-position  A flag to shuffle the positions before embedding to
                        the doc.
  -v, --version         show program's version number and exit
```

## Sample output

```
python main.py --epd-file 7men_human.epd --output-file sevenmen.docx --max-pos 10 --show-fen --show-bm --randomize-position --header "Seven-men test"
```

`sevenmen.docx`

![image](https://user-images.githubusercontent.com/22366935/202367172-72bac1f4-e190-4d77-82df-2d4fc5c201c5.png)




