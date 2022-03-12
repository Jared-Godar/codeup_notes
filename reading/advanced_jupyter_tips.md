## Jupyter / Markdown Guide

A few tips beyond the basic bold, italics, etc

### Page Break Lines

I knew about `---` but `***` and `___` do different styles of breaks

***

---

___

>Blockquotes
>>Up to 6 levels 
>>>Using `>`

### Highlighting code blocks

I knew you could use ``` for code blocks, but I didn't realize you could specify the language for formatting

```python
def fun():
    x=`some_python_shit`
return x
```

---

### Custom CSS

```markdown
<span style='color:green'> Python Programming</span>
<span style='color:Blue'> Machine Learning  </span>
## Changing Code Text Color
<code style="color:green;">i_am_green_var </code>
<code style="color:YOUR_COLOR_CHOICE;">
    data = [i for i in range(0,100)]
    print(data)
</code>
```

<span style='color:green'> Python Programming</span>
<span style='color:Blue'> Machine Learning  </span>
## Changing Code Text Color
<code style="color:green;">i_am_green_var </code>
<code style="color:YOUR_COLOR_CHOICE;">
    data = [i for i in range(0,100)]
    print(data)
</code>


#### Text Background Color

<span style='background:yellow'> Changing Text Background </span>
<span style='background :purple; color:white' > Changing Text Color and Background Both </span>

#### Font 

```markdown
<span style='font-family:Georgia'> It is Georgia font </span>
<span style='font-family:Verdana'> It is Verdana font </span>

<span style='font-size:36x; '> I am Big </span>
<span style='font-weight:500; '> I am Bolder </span>
```
<span style='font-family:Georgia'> It is Georgia font </span>
<span style='font-family:Verdana'> It is Verdana font </span>

<span style='font-size:36x; '> I am Big </span>
<span style='font-weight:500; '> I am Bolder </span>


#### Colored Note Boxes

- A Colored Note Boxes Is An Kind Of Message Box That Is Used To Display Some Sort Of Message With Predefined Styles.
- These Are Used To Get The User Attention Towards The Message Inside Them.
- There Are Mainly Four Type Of Alert Boxes
  - Alert-Info,
  - Alert-Success,
  - Alert-Danger,
  - Alert-Warning.

```markdown
<div class="alert alert-block alert-danger">
<b>Danger:</b> This is an example of danger colored box.</div>
<div class="alert alert-block alert-success">
<b>Success:</b> This is an example of success colored box.</div>
```

<div class="alert alert-block alert-danger">
<b>Danger:</b> This is an example of danger colored box.</div>
<div class="alert alert-block alert-success">
<b>Success:</b> This is an example of success colored box.</div>


### Tables

There Are Two Methods To Create Tables Inside Jupyter Notebook. First One Is By Using | As A Table Divide. The Second One Is With The Help Of <Table> </Table> Tag. You Can Use :-: For Centered, :- For Left Centered And — For Right Centered Table.

```markdown
| SN | Column A | Column B | Column C |
| :---: | :---: | :---: | :---: | 
| 0   | 10 | 11 | 100 |
| 1 | 22.5 | 23 | 23.5 |
```

| SN | Column A | Column B | Column C |
| :---: | :---: | :---: | :---: | 
| 0   | 10 | 11 | 100 |
| 1 | 22.5 | 23 | 23.5 |

### Links

[text](url)

### Images

![altname](path)

```markdown
<img src='https://victorzhou.com/media/nn-series/network.png' height="400" width="400"/>
```

<img src='https://victorzhou.com/media/nn-series/network.png' height="400" width="400"/>


### Navigation (Table of contents)

```markdown
Navigation Cell:-
<a Href="#Top">LINK TO TOP </a>
     Or 
[LINK TO TOP](#Top)

Target Cell:-
<span id='top' > SOME TEXT </span>
```

---

## Code Cells

Run shell commands inside notebook

```python
!pip install something
```

Can use `!` in front of line to run in terminal

`%%time` measures cell execution time

View documentation with `SHIFT+TAB`

### Alarm for cell execution 

```python
## YOUR CODE HERE
import winsound
duration = 5000   ## Means 5 Second
freq = 3600
winsound.Beep(freq, duration)
```

Remove extra output

```python
import warnings
warnings.filterwarnings('ignore')
```

## Embed videos

To Embed A Video On Your Jupyter Notebook You Need To Copy The `<iframe> </iframe> `Of The Video Instead Of URL.
You Can Find The Youtube Iframe Link In The Share > Embed.

```python
from IPython.display import HTML
HTML('<iframe>_URL_OF_THE_VIDEO')
```

### Keyboard shortcuts

KEYBOARD SHORTCUTS         USE
ESC + M                  Convert a Code Cell Into Markdown
ESC + B                  Insert a Code Cell Below
ESC + A                  Insert a Code Cell Above
SHIFT + ENTER            Run Current Cell
ESC + 1                  change cell to heading 1
ESC + 2                  change cell to heading 2
ESC + 3                  change cell to heading 3
ESC + 4                  change cell to heading 4
ESC + 5                  change cell to heading 5
ESC + 6                  change cell to heading 6
ESC + I                  Interrupt the kernel
ESC + 0                  Restart the kernel
Shift + Space            Scroll notebook up
Space                    Scroll notebook down
Tab                      Code completion or Indent
Shift + Tab              Tooltip 
Ctrl-]                   Indent
Ctrl-[                   Dedent 
Ctrl-/                   Comment
Ctrl-D                   Delete whole line 
Esc                      Enter command mode

### Convert Jupyter Notebook to SLideshow

Step 1: Click On View > Cell Toolbar > Slideshow To Convert Each Cell Into An Slide.

Step 2: Give Proper Slide Type To Each Cell By Choosing Between Slide, Sub Slide, Fragment, Skip And Notes

Step 3: Export It As Reveal.Js Slides By Navigating File > Download As > Reveal.Js Slides

Step 4: Open The Downloaded HTML To See The Slides In Action.