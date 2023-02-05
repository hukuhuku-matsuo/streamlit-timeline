![repo logo](https://github.com/innerdoc/streamlit-timeline/raw/main/component-logo.png)

# Timeline Component for Streamlit

A simple component to display a timeline in Streamlit apps. It integrates [Knightlab's TimelineJS](https://timeline.knightlab.com).


## Installation

First install Streamlit (of course!) then pip-install this library:

```bash
pip install streamlit
pip install streamlit-timeline
```


## Example

```python
# Streamlit Timeline Component Example

import streamlit as st
from streamlit_timeline import timeline


# use full page width
st.set_page_config(page_title="Timeline Example", layout="wide")

# load data
with open('example.json', "r") as f:
    data = f.read()

options = {
    "start_at_end": True,
    "is_embed": True
}

# render timeline
timeline(data, height=800, additional_options=options)
```


## Parameters

The `timeline()` function accepts a string or a dict, as long as it's in the [TimelineJS json format](https://timeline.knightlab.com/docs/json-format.html). The optional heigth of the visualization is in px.

## Options

For additional_option, [see here](https://github.com/NUKnightLab/TimelineJS#config-options)



## Preview
You can also check the [preview video](https://www.youtube.com/embed/N61ed-XvPR4) or go to the demo [A History of Natural Language Processing](https://github.com/innerdoc/nlp-history-timeline).

[![timeline example](https://github.com/innerdoc/streamlit-timeline/raw/main/example.png)](https://www.youtube.com/embed/N61ed-XvPR4)
