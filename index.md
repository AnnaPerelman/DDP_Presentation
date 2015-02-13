---
title       : Presentation of DDP Project
subtitle    : Understanding of Hemoglobin Blood Test Results
author      : 
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap, quiz, shiny, interactive]   # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
ext_widgets : {rCharts: [libraries/nvd3]}

---
        
## Background: understading our blood test's results
        
1. Nowadays all of us perform blood tests periodically
2. The very basic blood test is CBC - Complete Blood Count
3. One of the most important parameter coming up on this test is Hemoglobin level
4. Hemoglobin is the protein molecule in red blood cells that carries oxygen from the lungs to the body's tissues and returns carbon dioxide from the tissues back to the lungs
5. Understanding the meaning of Hemoglobin level is critical for taking some necessary
steps needed to keep patient's health on the needed level

---
        
## App Presentation
1. We'd like to introduce you an App that will help the patients to interpret their blood tests' results
2. The App needs user's input - the Hemoglobin level measured in gm/dl
3. As an output the App labels this number as "Low", "Normal" or "High" and gives some possible diagnosis.
4. Normal levels of Hemoglobin are between 11 and 14 gm/dl
5. Low (less than 11 gm/dl) Hemoglobin level is know as a result of anemia. So the App lets the user know that he is supposed to have anemia. This enables him to perform some preparation before his next meeting with his medical provider (family history, online research etc)
6. High (more than 14 gm/dl) Hemoglobin level can be seen in people living at high altitudes and in people who smoke. Dehydration produces a falsely high hemoglobin measurement which disappears when proper fluid balance is restored.
Some other infrequent causes are high hemoglobin levels are: advanced lung disease, certain tumors, a disorder of the bone marrow known as polycythemia rubra vera, and
abuse of the drug erythropoietin (Epogen) by athletes for blood doping purposes.

---

## This is how the application looks like.
Let's try to change the inputs and to see different outputs

<div class="row-fluid">
  <div class="container-fluid">
    <div class="row">
      <div class="col-sm-12">
        <h1>Hemoglobin Levels Analysis</h1>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-4">
        <form class="well">
          <div class="form-group shiny-input-container">
            <label for="Hemoglobin">Hemoglobin gm/dl</label>
            <input id="Hemoglobin" type="number" class="form-control" value="0" min="0" max="100" step="1"/>
          </div>
          <div>
            <button type="submit" class="btn btn-primary">Submit</button>
          </div>
        </form>
      </div>
      <div class="col-sm-8">
        <h3>Possible diagnosis</h3>
        <h4>You entered</h4>
        <pre id="inputValue" class="shiny-text-output"></pre>
        <h4>Which resulted in a possible diagnosis </h4>
        <pre id="prediction" class="shiny-text-output"></pre>
        <h5>App Documentation</h5>
        <h5>Here is an application designed to help patients 
                        taking blood test for hemoglobin levels to interpretate 
                        the results and to perform some preliminary steps needed 
                        to keep their health on a desired level.                           
                        The application is based on a patient input, 
                        which is a result of hemoglobin in blood test measured 
                        in gm/dl. Considering this input the application labels 
                        the results as "Normal", "Low" or "High".                           
                        In case the results are ubnormal (too low or too high)
                        the application gives a possible diagnosis which may help
                        the patients in finding the appropriate medical provider 
                        for their case.</h5>
      </div>
    </div>
  </div>
</div>

--- 
## Further Development
1. This application may be upgraded with the additional input parameters such as an age, smoking status, family history etc
2. The same way the application may examine glucose, calcium and many other components of blood tests.





