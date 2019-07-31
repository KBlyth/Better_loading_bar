# Better_loading_bar


"Add a full-featured loading bar to any loop type and process in just two lines!"


**Better_loading_bar** is a single script, multi-function and multi-option class meant to allow for easy setting up and tracking of tasks progress. 

Integration is kept as simple as possible, while giving the user full access to a significant number of usefull information such as ETA, run time, completion, etc... The progress bar also contains an **activity indicator**, which allows for easy determination of ongoing processes existance (useful for long loops).

The bar can be used for *while* loops too. This allows to provides information and insight on the iterations (providing run_time, and tota run time for example).

The progress bar can be run on a single line in the or can update over new lines as process proceeds (to allow for information to be printed in between).

The bar is fully customisable, just set to *False* all unwanted information and parameters at initiation. Various bar and activity tracker designs are available for optimal visual effects.

ANSI colours are used to enhance readability, but require compatible install to be visible (progress bar will work regardless). A special **Rainbow mode** is available for maximum visibility!

### Progress bar:

Progress bars are used to keep track of pre-defined length processes. To create a progress bar, simply initiate an instance of the progress bar (specify the wanted information there, max_step must be specified).

```python
bar =  Progress_bar(max_step=30)
```

Run `.update_progress` to update progress (for loops) or `.update_activity` to keep the activity animations going between main progress updates (when minor progress is made).

*Tips: In case of very quick loops, disable "activity_indicator" 

### Activity bar

Activity bars are used to keep track of unknown-length processes (while loops).
To create an activity bar, simply initiate an instance of the progress bar (specify the wanted information there, keep max_step to None):

```python
bar =  Progress_bar(max_step=None)
```

Run `.update_activity` at the end of every iteration to update activity.
