# EducationPerfected

#### Javascript user-script to automatically answer Education Perfect language questions at **high** speeds.

Works for word-word (translation) tasks and Dash mode.  
**Does not work with Audio-tasks, YET.** <br><br>

### **Read this then read the README inside v2 folder [here](https://github.com/KEN-2000l/EducationPerfected/tree/main/v2)**

![example image](result.png)

## Usage

### Loading/installing the script

The script or program itself is in `script.js`. Click `script.js` above amongst the files to get the code.  
This script works by being "injected" into, or to execute on top of, a webpage (with Education Perfect open).  
**There are two main ways to inject this script:**

- **One-time; console**:  
  Paste the script contents into the DevTools (aka inspect mode) console on a Education Perfect page. (Then press enter, and you can close the DevTools panel.)  
  <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>I</kbd> is a standard keybind to open DevTools, and the console is one of the tabs usally located at the top.  
  This is a manual and temporary solution; you will have to manually re-inject each time you open/refresh the Education Perfect page.

- **Auto-load; browser extension (Recommended)**:  
  A browser extension designed to manage such scripts can automatically inject the script in the background each time you load the page. One such extension is called [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo).  
  Install Extension >> Open extension popup/menu (by clicking its icon) >> Click `Create a new script...` >> Delete all template code >> paste the script in >> <kbd>Ctrl</kbd> + <kbd>S</kbd> to save >> (Close editor) >> Script will autoload when you load Education Perfect each time (refresh to load if you the page already open)

  _Note: use [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887) on Safari as Tampermonkey is paid there._

### Hotkeys

Upon loading/injecting, the script does not do anything. **All functions are triggered via _hotkeys/keybinds_ as listed below:**

- **Load/Refresh Word List -> <kbd>Opt/Alt</kbd> + <kbd>R</kbd>:**  
  _To be used on task-starter page with list of words and translations_  
  Scrapes the translations displayed and utilizes that information to answer questions.  
  For it to correctly answer all questions, make sure to refresh the word list before each new task.

- **Semi-Manual Answer -> <kbd>Opt/Alt</kbd> + <kbd>A</kbd>:**  
  _To be used on a running task's page (after clicking start)_  
  Finds the answer for each question and copies it to your clipboard.  
  You can then simply press <kbd>Ctrl/Cmd</kbd> + <kbd>V</kbd> to paste it into the answer box (and press enter to submit).

- **Fully-Auto Answer -> <kbd>Opt/Alt</kbd> + <kbd>S</kbd>:**  
  _To be used on a running task's page (after clicking start)_  
  Finds the answer for each question and automatically enters it and submits it. (Completes a task mode fully-auto; how wonderful!)  
  It has been optimized for maximal speed!

  _Note: You can also pause the auto-answer midway by pressing the hotkey again._

### Extras

#### Feature-Explanation

- **Full Speed Auto Answer:**  
  The current speed is the maximum achievable so far. It will probably not be possible to go faster without a different concept.
- **Self-Learning/Error Correction:**  
  When an error is made (due to bad question/answer parsing, lag, or missing word list), the script handles the popup and extracts the corret answer information to stop making the same mistake again (hopefully).  
  The incorrect answer popup has a normal delay of 3 seconds before you can close it, but that's slow so it instead gets delyeeted :P
- **Smart-ish Word Parsing:**  
  A big source of incorrect answers is when no answer is found due to unsatisfactory matching (of the question to an answer).  
  Education perfect is annoying in the sense of having really bad formatting standards. The entries on the word list can be dislayed differently as a question (and there are many different edge cases). The script handles _most_ of these edge cases, and for those that still fail to match, the self-learning function will take care of that in _most_ of the remaining scenarios. There are still extreme cases of really bad formatting (such as commas with repeated words and blatant disparities between displayed answer and expected answer) where a question may not get correctly answered. These should also get fixed soon.

## `script+.js`

_In Beta; currently broken_

### Note: this script is very much a wip as of now, and will most likely have a few issues that you'll encounter. If you notice any, please report them [here](https://github.com/KEN-2000l/EducationPerfected/issues/12) :D

#### Even-more-automated version of the standard: self-navigation between tasks to run AFK

Has one hotkey of <kbd>Opt/Alt</kbd> + <kbd>S</kbd>. Usable in three contexts: Task-starter page with word list, _language_ subject homepage, or folder/directory in the subject content browser.  
When the hotkey is pressed, it will explode your mind by completing as many tasks as it can depending on the activation context:

- Subject homepage => everything in the subject
- Content browser => everything within the current folder
- Task-starter page => this task

#### _By [Garv](https://github.com/garv-shah) and [KEN_2000](https://github.com/KEN-2000l)_
