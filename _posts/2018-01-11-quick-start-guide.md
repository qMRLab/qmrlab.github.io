---
layout: post
title:  "Quick Start Guide"
author: sal
categories: [ Jekyll, tutorial ]
image: assets/images/12.jpg
featured: true
hidden: true
---
 

 <script type="text/javascript"
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.2/MathJax.js?config=TeX-MML-AM_CHTML">
 </script>
<script type="text/x-thebe-config">
      {
      	requestKernel: true,

        bootstrap: true,
        selector: "pre",
        binderOptions: {
        repo: "agahkarakuzu/sosExample",
        ref: "master"
        },

        kernelOptions: {
    	name: "SOS"
     	},
  
        
      }
    </script>
<script type="text/javascript" src="https://unpkg.com/thebelab@^0.3.0"></script>



You want to run interactive jupyter notebooks in a blog post? It's never been easier. 
 
Here is an example:

Kernel Status: <span class="thebe_status_field"></span>


<pre data-executable="true" data-language="octave">
%use octave
t = 0:0.01:10;
</pre>



<pre data-executable="true" data-language="octave">
%use Python3
%get t --from Octave
import plotly
import plotly.plotly as py
import plotly.graph_objs as go
import numpy as np
from plotly import __version__
from plotly.offline import download_plotlyjs, init_notebook_mode, plot, iplot
plotly.tools.set_credentials_file(username='TommyBoshkovski', api_key='L93ChErVewlTwok2buNM')
#init_notebook_mode(connected=True)

data = [dict(
        visible = False,
        line=dict(color='#00CED1', width=6),
        name = '𝜈 = '+str(step),
        x = t,
        y = np.sin(step*np.arange(0,10,0.01))) for step in np.arange(0,5,0.1)]
data[10]['visible'] = True

steps = []
for i in range(len(data)):
    step = dict(
        method = 'restyle',  
        args = ['visible', [False] * len(data)],
    )
    step['args'][1][i] = True # Toggle i'th trace to "visible"
    steps.append(step)

sliders = [dict(
    active = 10,
    currentvalue = {"prefix": "Frequency: "},
    pad = {"t": 50},
    steps = steps
)]

layout = dict(sliders=sliders)

fig = dict(data=data, layout=layout)

py.iplot(fig, filename='Sine Wave Slider')
</pre>


<pre data-executable="true" data-language="octave">
%use octave
% This part is for qMRLab
startup;
qMRgenBatch(mt_ratio,pwd);
% If you run mt_ratio_batch, fit will happen but inline plot will fail. Octave & imshow issues. 
% But we can transfer this to the Python and display it with Plotly.. later...
</pre>
