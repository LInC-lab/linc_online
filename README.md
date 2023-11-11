# linc_online
Experiments and utilities for running experiments online

## Modifying a pre-existing plugin
- Download the existing plugin that you would like to modify (most likely .ts)
  - https://github.com/jspsych/jsPsych/tree/main/packages/plugin-image-button-response
- Make a new folder in our repo folder /dev_testing/, this is where you will create an html file to test the custom plugin
  - You can duplicate the /free_sort_example/ folder, just rename it
- Duplicate the custom_plugin_template.js in our github repo, rename it to something descriptive
- In your new .js file, rename jsPluginName to the new name
- For the following, you may have to change the format from TypeScript to JavaScript
  - Either manually or use ChatGPT, just be sure to check and read through everything. Pay attention to the details.
- Modify the const info
  - You’ll most likely be able to just copy over the const info = {} section from the original plugin
  - However, make sure that the type: section matches that in the custom_plugin_template (i.e., type: jspsych.ParameterType. etc.)
  - If you need to add a new parameter, do so here.
- (Optional) update the comments, author, etc.
- Modify the plugin
  - Again, copy the converted js code to this section, ensuring that all of the names are correct.
  - It’s convenient to use a pre-existing function since it will have great formatting and already has a data format to save.
  - Modify whatever you need
    - For the text image button response example, I reorganized the ordering of the html concatenation (two spots), so that it goes text, image, button instead of image, button, text
- Back in the /dev_testing/ folder, try out the new custom plugin with a basic html file. 
  - The free_sort_example html has the correct and up-to-date jspsych imports at the top.
  - The structure will also be the same.
