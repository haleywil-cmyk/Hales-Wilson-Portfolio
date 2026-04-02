| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

#  Critique and redesign (MakeoverMonday)

_For each step below, you should document your progress as you move forward.  In terms of tone, think of the writeup as though you're keeping journal of your step-by-step process.   You should include a any insights you gained from the critique method, and what it led you to think about when considering the redesign.  You should talk about how you moved next to the sketches, and any insights you gleaned from your user feedback.  Document what you changed based on the user feedback in your redesign.  Finally, talk about what your redesigned data visualization shows, why you selected the data visualization you did, and what you attempted to show or do differently._

_You can include screenshots, sketches or other artifacts with your narrative to help tell the story of how you moved through the process.  Again, make sure to avoid including any personally identifying information about your interviewees (don't list full names, etc.).  While this template serves as a guide, make sure to reference the assignment writeup on Canvas for the official guidance.  This template does not include all guidance mentioned on the assignment page._

## Step one: the visualization

_Include link to the original data visualization (or screenshot - make sure to correctly cite your sources, etc.).  Include paragraph or two on why you selected this particular data visualization.  For obvious reasons, the data visualization you select should come from a publicly accessible source._

Global Slavery Index:
https://www.walkfree.org/global-slavery-index/#:~:text=An%20estimated%2050%20million%20people,10%20million%20people%20since%202016 .
<img width="1568" height="737" alt="image" src="https://github.com/user-attachments/assets/36e93c09-4a8a-4f3e-bc7b-9922c00d618f" />


## Step two: the critique

The number of products stood out to me first as the key was color-coded and had corresponding symbols. I thought the graph did well in telling me which of the G20 countries spend the most money on imports derived from modern slave labor. This was done in ascending ranking order. At first, I thought the stacked bar graph was a little jumbled, and didn't show the proportion of country spending to the product. This specific graph of many visualizations did not have a title, so it took reading supporting paragraphs to understand what was being presented.

I think the primary audience for this tool is individuals in global leadership positions, such as CEOs of corporations and politicians, who would be able to combat countries' roles in modern slave labor. I think it is definitely effective in showing the correlation between a country's spending and the overexploitation of its underdeveloped countries' resources. Additionally, I think the data visualization could also appeal to smaller communities to inform them about how modern-day luxuries are obtained and to rally support for ending modern slavery.

For some reason, I really like using a map visualization and will try to use that to show how the 20 different countries are complicit in modern slavery. I think I would also want to show that different countries invest more in different products.

## Step three: Sketch a solution
<img width="2246" height="2900" alt="image" src="https://github.com/user-attachments/assets/e9cdfe66-6bcb-4ae4-a74b-14db1b5b28b7" />

## Step four: Test the solution

_Before you conduct your interviews, prepare a simple script.  Use this as a guide and as a way to take notes as you go forward. Come up with your own list of questions you want to ask for the selected visualization. Keep the questions broad so you can get the most value out of your feedback. Then, document answers to your questions here._

Questions to ask (modify these for your own interviews): 

- Does a map work well with telling this data-driven story?
- Can you understand the relation of the countries to the items?
- What could make the design clearer?
- Do you have any other suggestions for visualization?


Results: 

_Don't identify or share personally identifiable information (PII) about the people you spoke to._


| Question | Interview 1: MAM, Late 20s | Interview 2: ARCH(UG), Early 20s |
|----------|-------------|-------------|
|Does a map work well with telling this data-driven story?         | Thinks a map concept would be interesting and eye-catching for the audience              |Agrees original stacked bar graph is a little confusing and relies heavily on guided labels           |
|Can you understand the relation of the countries to the items?          |Could tell in the sketch that the size of the circle represents to the amount each country invested/spent   |Recognized some countries having different relationship to products but not really shown|
|What could make the design clearer?          |Thought it would be interesting to show how different countries fund a variety of products              | Brought up the idea of highlighting countries with interesting data rather than all of them     |

Synthesis: 

_What patterns in the feedback emerge?  What did you learn from the feedback?  Based on this feedback, come up with what design changes you think might make the most sense in your final redesign._

My critique group felt that the original visualization was overwhelming and did not properly convey the spending ratios of smaller countries relative to their imports. They agreed that a redesign could better highlight the variety of data across countries and products. They also suggested exploring a treemap with circles as an alternative if the symbol map approach did not come together cleanly.

## Step five: build the solution

_Include and describe your final solution here. It's also a good idea to summarize your thoughts on the process overall. When you're done with the assignment, this page should all the items mentioned in the assignment page on Canvas(a link or screenshot of the original data visualization, documentation explaining your process, a summary of your wireframes and user feedback, your final, redesigned data visualization, etc.)._

I chose this dataset because it was a topic that genuinely interested me and one I wanted to encourage others to research. The Global Slavery Index data felt important and I thought a strong visualization could be a way to draw people in. I also just really like map visualizations. Anytime I'm comparing countries, my instinct is always to reach for a map, so this felt like a natural fit. My original idea was to create circles sized by import value (in thousands USD) hovering over their respective countries. This led me to experiment with both the symbol map and filled map options in Tableau to see which would work better as a base.

Things got complicated quickly. One of the first problems I ran into was that when I tried to display which product each country spent the most money on, it would no longer show the total amount from the original graph. I worried this would confuse anyone reading the visualization, since losing that total value would not match the orginal graph. Something else I hadn't fully factored in was that several countries, like China, Brazil, and Argentina, appeared in the data as both importers and origin countries. I tried using a filter to remove G20 countries from the origin country layer, but this ended up affecting the value amounts, which created a whole other problem.
I also really wanted to create an overlay of lines connecting importer countries to their origin countries, but every time I tried, the lines would connect in weird jagged edges on the same layer. I eventually realized that doing this properly would require editing the underlying data itself, which was more than I could take on at that point.

<img width="1532" height="784" alt="image" src="https://github.com/user-attachments/assets/cc779348-8dd2-43ac-836a-a62886d603ea" />

All of these roadblocks forced me to step back and think about what story I was actually trying to tell. Since I had spent so much time working with the map format, I wanted to stick with it and just simplify what I was trying to show. I landed on focusing on which countries spent the most on imports, using a single green color gradient on the filled map (green = money was the connection I wanted to make), with the total amount visible when you hover over a country. I kept a second layer showing origin countries and their products, which still had some of the overlap issues, but was less visually distracting than my earlier attempts.

I also went back and forth on the title, specifically whether to include the words "modern slave labor" directly. I ultimately decided against it because I didn't want to undersell the severity of the issue, and I felt the phrasing I landed on still communicated the weight of the topic. The dark background was a last-minute change to add more contrast, though in hindsight I think I could have explored more options there.

Honestly, this visualization did not come together 100% the way I envisioned. The data has so many overlapping variables, with countries playing dual roles, multiple products, and values at different scales, that it was genuinely difficult to show everything cleanly in one view. Had I had more time, I would have liked to figure out the connecting lines between countries, which I think would have made the geographic relationships much clearer and more compelling. But I am glad I stayed with the map format because I think it still communicates the core message better than a bar chart would. You can see the scale of this problem geographically in a way that a list of numbers just does not capture.

  # G20 Spending on Modern Slave Labor by Country and Product
  <div class='tableauPlaceholder' id='viz1775101681923' style='position: relative'><noscript><a href='#'>
    <img alt='G20 Spending on Modern Slave Labor by Country and Product ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;8H&#47;8HDZ6TPB3&#47;1_rss.png' style='border: none' /></a></noscript>
    <object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> 
      <param name='embed_code_version' value='3' /> 
      <param name='path' value='shared&#47;8HDZ6TPB3' /> 
      <param name='toolbar' value='yes' />
      <param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;8H&#47;8HDZ6TPB3&#47;1.png' /> 
      <param name='animate_transition' value='yes' />
      <param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' />
      <param name='display_overlay' value='yes' />
      <param name='display_count' value='yes' />
      <param name='language' value='en-US' />
      <param name='filter' value='publish=yes' />
    </object>
  </div>                
  <script type='text/javascript'>
    var divElement = document.getElementById('viz1775101681923');                    
    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
    var scriptElement = document.createElement('script');                    
    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                
  </script>

## References
_List any references you used here._

_Walk Free. (2023). Global Slavery Index 2023. Minderoo Foundation. https://www.walkfree.org/global-slavery-index/

## AI acknowledgements
_If you used AI to help you complete this assignment (within the parameters of the instruction and course guidelines), detail your use of AI for this assignment here._

I used Claude (Anthropic) throughout this project to help troubleshoot my Tableau build and think through design decisions in real time. I asked questions about how to structure my marks layers, why my map was rendering incorrectly, and how to handle countries appearing in both importer and origin roles. All final decisions and the visualization itself were made and built by me in Tableau.

-
