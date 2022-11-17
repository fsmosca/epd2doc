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
 
 With requirements.txt file, you can also install the requirements with:
 
 ```
 pip install -r requirements.txt
 ```
  
## Command line

```
python main.py --epd-file 7men_human.epd --output-file sevenmen.docx --max-pos 10 --show-fen
```

## Help

```
python main.py --help
```

See [wiki](https://github.com/fsmosca/epd2doc/wiki/Help).

## Sample output

`command line`

```
python main.py --epd-file 7men_human.epd --output-file sevenmen.docx --max-pos 10 --show-fen --show-bm --randomize-position --header "Seven-men test"
```

`sevenmen.docx`

![image](https://user-images.githubusercontent.com/22366935/202367172-72bac1f4-e190-4d77-82df-2d4fc5c201c5.png)




