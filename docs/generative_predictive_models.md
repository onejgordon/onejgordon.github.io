---
title: Generative Predictive Models
layout: page
---

<section class="medium" data-field="body" class="e-content">
<section name="b8c9" class="section section--body section--first"><div class="section-divider"><hr class="section-divider"></div><div class="section-content"><div class="section-inner sectionLayout--insetColumn"><h3 name="6d7b" id="6d7b" class="graf graf--h3 graf--leading graf--title">An illustrated overview of how our brains (might) think — the fascinating intuition of the generative predictive model</h3><blockquote name="c4b7" id="c4b7" class="graf graf--pullquote graf--startsWithDoubleQuote graf-after--h3">“Perception is controlled hallucination.” </blockquote><blockquote name="4b8c" id="4b8c" class="graf graf--pullquote graf-after--pullquote"> — Andy Clark</blockquote><p name="cab9" id="cab9" class="graf graf--p graf-after--pullquote">Paradigm shifts are rare and incredible events. I recently came across an idea that prompted such a shift: introduction to a modern unified theory of perception. Specifically,  that<strong class="markup--strong markup--p-strong"> our brain’s primary function  is to reduce surprise by developing an increasingly nuanced model of the world. </strong>It is constantly predicting the future (on multiple time scales), noticing incorrect predictions, and updating its model to explain away the difference. </p><p name="d528" id="d528" class="graf graf--p graf-after--p">Before I came across any of these ideas, I had no sense of the current state of the science around perception and consciousness. Now that I’ve seen the tip of the iceberg, I‘ve begun to believe that modern theories of mind across multiple disciplines (psychology, neuroscience, data science &amp; machine learning, not to mention multiple schools of philosophical thought) are beginning to resolve into something that feels much more unified, and surprisingly intuitive. By definition, perception mediates every aspect of human experience, and so any changes to the way we understand perception comes with a huge breadth of implications (which I would argue extend beyond the personal to the societal).</p><p name="b84e" id="b84e" class="graf graf--p graf-after--p">These theories come with many names, but I find Andy Clark’s term ‘generative predictive model’ most descriptive. As a disclaimer, much of the below is still speculative theory, though theory supported by a growing body of evidence, so only the future will inform us of the specific errors in this paradigm itself (meta!). My purpose here is to visually share the basics of my understanding in case others who haven’t seen these ideas may find them similarly intriguing. </p><h4 name="9223" id="9223" class="graf graf--h4 graf-after--p">Building Blocks — Neurons and Spikes</h4><p name="9f18" id="9f18" class="graf graf--p graf-after--h4">We’ve been aware of the significant role of neurons in how brains (and the entire nervous system) work since the 1800’s (!), thanks to the work of <a href="https://en.wikipedia.org/wiki/Santiago_Ram%C3%B3n_y_Cajal" data-href="https://en.wikipedia.org/wiki/Santiago_Ram%C3%B3n_y_Cajal" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">Santiago Ramon y Cajal</a>, sometimes known as the father of modern neuroscience.</p><p name="d488" id="d488" class="graf graf--p graf-after--p">Those looking to understand the neuron in order to analyze and predict its function have created an array of simplified models that abstract away some or all of the lower level biochemical dynamics. Artificial neural networks, and their modern evolution, deep learning (and deep reinforcement learning), are a category of machine learning techniques that has brought to the world increasingly impressive computational feats (e.g. beating humans at <a href="https://www.theguardian.com/global/2015/may/13/baidu-minwa-supercomputer-better-than-humans-recognising-images" data-href="https://www.theguardian.com/global/2015/may/13/baidu-minwa-supercomputer-better-than-humans-recognising-images" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">image recognition</a>, <a href="https://en.wikipedia.org/wiki/Deep_Blue_%28chess_computer%29" data-href="https://en.wikipedia.org/wiki/Deep_Blue_(chess_computer)" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">Chess</a>, <a href="https://deepmind.com/research/alphago/" data-href="https://deepmind.com/research/alphago/" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">Go</a>, <a href="http://www.nature.com/nature/journal/v518/n7540/abs/nature14236.html" data-href="http://www.nature.com/nature/journal/v518/n7540/abs/nature14236.html" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">old-school video games</a>, and <a href="https://www.riverscasino.com/pittsburgh/BrainsVsAI/" data-href="https://www.riverscasino.com/pittsburgh/BrainsVsAI/" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">Texas Hold-em</a>, among others). These networks are built from a vastly simplified neuron that does nothing more than take a bunch of inputs, perform some addition and multiplication, and pass them on. In these cases, of course, it is the structure of the network (the way the neurons are connected) and the algorithm by which these networks learn, that enable advanced capabilities.</p><figure name="64a0" id="64a0" class="graf graf--figure graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 700px; max-height: 365px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 52.1%;"></div><img class="graf-image" data-image-id="1*sUr2ejGON4T-2LdFQemDig.png" data-width="800" data-height="417" src="https://cdn-images-1.medium.com/max/1600/1*sUr2ejGON4T-2LdFQemDig.png"></div><figcaption class="imageCaption">Three views of a neuron. Left: real neuron, calcium imaging, center: illustration, right: schematic.</figcaption></figure><p name="f982" id="f982" class="graf graf--p graf-after--figure">In reality, an incredibly complex system of biochemical pathways are at work in any given neuron, but it can be useful to zoom out a bit, and view neurons as information processing units. </p><p name="3a31" id="3a31" class="graf graf--p graf-after--p">Information is passed in from other neurons as voltage spikes through the vast branching network of roots (dendrites), and moves towards the cell body. If the right concurrence of these signals arrives at the right time, the cell will be activated, and pass on this voltage spike down its axon (the main outgoing channel which can be up to a meter in length for motor neurons), to the dendrites of other downstream neurons.</p><figure name="e902" id="e902" class="graf graf--figure graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 500px; max-height: 205px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 41%;"></div><img class="graf-image" data-image-id="1*SmP8mXZ5RV0EBkz8R2xFuQ.gif" data-width="500" data-height="205" src="https://cdn-images-1.medium.com/max/1600/1*SmP8mXZ5RV0EBkz8R2xFuQ.gif"></div><figcaption class="imageCaption">Propagation of action potential (voltage spike) down an axon</figcaption></figure><p name="6d98" id="6d98" class="graf graf--p graf-after--figure">The neuron’s anatomy allows it to precisely detect patterns, possibly many thousands distinctly, and pass on their detection to any other neurons it is connected with.</p><h4 name="5d4b" id="5d4b" class="graf graf--h4 graf-after--p">Hierarchy</h4><p name="3d71" id="3d71" class="graf graf--p graf-after--h4">There is good evidence that our neocortex (the millimeters thick dinner-napkin sized sheet of tissue that evolved most recently in mammal brains) is organized hierarchically, with the lower levels handling raw sensory input — data from our eyes, ears, nose, skin, muscles, etc — and each higher region taking inputs from the outputs of the regions below. There is also evidence that each region, regardless of which senses it receives information from, is performing exactly the same kinds of processing: <strong class="markup--strong markup--p-strong">A) finding and encoding relevant structure</strong> in its inputs, <strong class="markup--strong markup--p-strong">B)</strong> <strong class="markup--strong markup--p-strong">building a model</strong> to explain the structure seen, and using this model to <strong class="markup--strong markup--p-strong">C)</strong> <strong class="markup--strong markup--p-strong">predict future events</strong>. </p><h4 name="7334" id="7334" class="graf graf--h4 graf-after--p">A) Finding Structure (pattern recognition)</h4><p name="fcff" id="fcff" class="graf graf--p graf-after--h4">In the nomenclature of Hawkins et al at Numenta, finding structure is a process of spatial pooling. Individual neurons in a region (as introduced above) <em class="markup--em markup--p-em">learn</em> spatial patterns of incoming inputs. For example, a neuron can learn to detect the coincidence of a few thousands incoming messages from the region below. It does so by learning associations over time. There are multiple mechanisms by which this learning occurs, and the actual algorithms our biology uses are a topic of debate and present research, but a basic form called Hebbian Learning occurs when ‘neurons that fire together, wire together’.</p><figure name="83f7" id="83f7" class="graf graf--figure graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 700px; max-height: 313px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 44.7%;"></div><img class="graf-image" data-image-id="1*Uv22jYtiJqacAIf9-U5xvw.png" data-width="936" data-height="418" src="https://cdn-images-1.medium.com/max/1600/1*Uv22jYtiJqacAIf9-U5xvw.png"></div><figcaption class="imageCaption">Finding structure in a hierarchically lower region. In this simple example, the highlighted cell takes input from three neurons in the region below, and therefore activates when a pattern involving those 3 cells is detected. Following diagrams represent cells and regions in 2D, as shown on the right.</figcaption></figure><p name="bfbc" id="bfbc" class="graf graf--p graf-after--figure">In the above diagram, if neurons <em class="markup--em markup--p-em">a</em>, <em class="markup--em markup--p-em">b</em> and <em class="markup--em markup--p-em">c</em> consistently fire together over time, their connections to <em class="markup--em markup--p-em">d </em>(in region 2) will strengthen, and as a result <em class="markup--em markup--p-em">d</em> will learn to represent or summarize this feature of the activity in region 1. Because each of the neurons in region 2 learns to represent similar coincidences (or more complex patterns) representing all the patterns seen in R1, R2 forms a representation of its inputs using fewer neurons. In the data science world this is called dimensionality reduction, and it means that the region has efficiently encoded the information coming in.</p><figure name="9bef" id="9bef" class="graf graf--figure graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 284px; max-height: 343px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 120.8%;"></div><img class="graf-image" data-image-id="1*s9cGEj8BGsGc2hSZoNc-WA.gif" data-width="284" data-height="343" src="https://cdn-images-1.medium.com/max/1600/1*s9cGEj8BGsGc2hSZoNc-WA.gif"></div><figcaption class="imageCaption">Feed forward pattern detection. The cell in the top region is setup to be activated by brightness in the top of the image, and inhibited by brightness at the bottom. Result: ultra simplified detection of images that are bright at top and dark on bottom. (Key — green: active excitatory neuron, red: active inhibitory neuron, gray/white: inactive, rings: spatial source or ‘receptive field’ of each cell, each ring passes the brightness from that section of the image to the cell above it)</figcaption></figure><p name="3ce4" id="3ce4" class="graf graf--p graf-after--figure">The illustration above demonstrates the way these feed-forward connections can allow a higher region to ‘summarize’ the raw activity below in a more abstract representation. As a direct result of this abstraction, these representations change less frequently over time, and as such are called <em class="markup--em markup--p-em">invariant representations</em>. In the words of Hawkins:</p><blockquote name="7f2f" id="7f2f" class="graf graf--blockquote graf--startsWithDoubleQuote graf-after--p">“Each region of the cortex learns sequences, develops what I call ‘names’ for the sequences it knows, and passes these names to the next region higher in the cortical hierarchy … This ‘name’ is a group of cells whose collective firing represents the set of objects in the sequence … By collapsing predictable sequences into ‘named objects’ at each region in our hierarchy, we achieve more and more stability the higher we go. This creates invariant representations.” </blockquote><blockquote name="0e1d" id="0e1d" class="graf graf--blockquote graf-after--blockquote">— Hawkins, On Intelligence</blockquote><p name="ba8c" id="ba8c" class="graf graf--p graf-after--blockquote">To illustrate this, imagine we are scanning a scene, and our eyes saccade (rapidly move from one point to another) between small pieces of the scene. Imagine our scene contains a dog and a tree, each with a number of its own features.</p><p name="dd92" id="dd92" class="graf graf--p graf--empty graf-after--p"><br></p><figure name="d3ac" id="d3ac" class="graf graf--figure graf--layoutOutsetLeft graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 500px; max-height: 390px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 78%;"></div><img class="graf-image" data-image-id="1*xxYa_k6sr7YaDynskfE9Hg.gif" data-width="500" data-height="390" src="https://cdn-images-1.medium.com/max/1200/1*xxYa_k6sr7YaDynskfE9Hg.gif"></div><figcaption class="imageCaption">Feed-forward invariant representation.</figcaption></figure><p name="0402" id="0402" class="graf graf--p graf-after--figure">At left, we have cells that have learned to represent ‘dog’ sensory inputs (underlined with gold), and those that have learned the features of ‘tree’ (underlined in green). The top region in the hierarchy stays active while any of its learned inputs are active. Here the input object (the thing in our view) is alternating between tree and dog, and during each, encodings (bottom layer) of its features are randomly iterated (e.g. as the observer scans the object).</p><p name="09a9" id="09a9" class="graf graf--p graf-after--p">Just as neuroscientists identified a <a href="http://www.nature.com/nature/journal/v435/n7045/full/nature03687.html" data-href="http://www.nature.com/nature/journal/v435/n7045/full/nature03687.html" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">‘Bill Clinton’ neuron</a> in the minds of study participants, the top right neuron in this illustration activates when our network is exposed to a dog.</p><h4 name="7fee" id="7fee" class="graf graf--h4 graf-after--p">B) Modeling &amp; Prediction</h4><p name="355a" id="355a" class="graf graf--p graf-after--h4">Detecting patterns and structure in the region below is one important step in model-building, but to build a model based solely on present sensory input would be to ignore all the cues of present context, and the history that led to the present moment. That’s why actual brain regions are deeply recurrent — they take inputs not only from below, but also receive extensive feedback from regions above, as well as lateral inputs from other cells in the same region. </p><figure name="df49" id="df49" class="graf graf--figure graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 700px; max-height: 700px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 100%;"></div><img class="graf-image" data-image-id="1*kXyPc-XmmqMIQll7i2UINA.png" data-width="720" data-height="720" src="https://cdn-images-1.medium.com/max/1600/1*kXyPc-XmmqMIQll7i2UINA.png"></div></figure><p name="28b4" id="28b4" class="graf graf--p graf-after--figure">Our brains are well adapted for perpetually noisy and incomplete information, and as a result, we aggressively extrapolate and interpolate hints from our senses into complete pictures (models) of our environment. Going back to a previous example, if a higher region has built a model of its environment that includes ‘dog’, it likely does two things:</p><ol class="postList"><li name="7b8d" id="7b8d" class="graf graf--li graf-after--p">It biases other cells in the same region (and thus at a similar level of abstraction) via historical associations that have learned probabilistic links to ‘dog’. Perhaps in 30% of recent situations where we perceived dog, we were  also in a park. These biases might prime certain networks of cells in the region (learned patterns such as ‘frisbee’, ‘grass’, ‘picnic blanket’) to be more likely to activate.</li><li name="5019" id="5019" class="graf graf--li graf-after--li">This group of associated patterns in a region passes down contextual feedback, in the form of predictions or expectations, to lower regions. If this brain region could talk, it may say: “I’m perceiving a dog, so lower auditory region, you may experience a bark, and lower visual region, you may see a tail or a collar”.</li></ol><p>From Clark:</p><blockquote name="b181" id="b181" class="graf graf--blockquote graf--startsWithDoubleQuote graf-after--li">“…naturally intelligent systems do not passively await sensory stimulation. Instead, they are constantly active, trying to predict (and actively elicit…) the streams of sensory stimulation before they arrive. Before an ‘input’ arrives on the scene, these pro-active cognitive systems are already busy predicting its most probable shape.”</blockquote><blockquote name="5dd3" id="5dd3" class="graf graf--blockquote graf-after--blockquote"> — Clark, Surfing Uncertainty</blockquote><h4 name="18f5" id="18f5" class="graf graf--h4 graf-after--blockquote">Information as Error</h4><p name="a7af" id="a7af" class="graf graf--p graf-after--h4">Clark offers a number of compelling arguments explaining that the information traveling up through the hierarchy may be more efficiently encoded as surprise — deviations from expectation — rather than pure positive information. Various forms of this prediction error mechanism have gained traction, and notably, the <a href="http://www.thebrainprize.org/flx/prize_winners/the_brain_prize_winners_2017/" data-href="http://www.thebrainprize.org/flx/prize_winners/the_brain_prize_winners_2017/" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">2017 brain prize</a> went to three researchers focused on, among other things, demonstrating the role of dopamine in <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4826767/" data-href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4826767/" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">communicating prediction error</a>.</p><p name="d961" id="d961" class="graf graf--p graf-after--p">Conveniently, this paradigm matches intuition on how one might design an instrument like the brain to efficiently encode a changing world. Since the state of the world tends to change smoothly (and rarely abruptly), much of our perception at any given moment in time is similar to what we experienced (saw, heard, felt) at the previous moment. A favorite illustration for this is that the efficiency derived from this approach is heavily leveraged in video streaming software. Imagine the data required for your favorite streaming service to show a few frames of video of a hawk flying through a blue sky. Rather than transmit the color of each pixel of your screen (mostly blue, still mostly blue, still mostly blue), many times per second, it transmits only the changes from the previous frame (perhaps a handful of pixels become  brown and black in front of the hawk, and blue behind). </p><p name="da42" id="da42" class="graf graf--p graf-after--p">As we’ve seen, unlike video services, which know very little about the meaning of what they’re displaying, each region of our brain leverages its model of the dynamics of the world to predict the incoming stream of information. As we watch a hawk cross the sky, our model tells us that this is an object in front of a distant background moving to the right. Each level of hierarchy already has its predictions for exactly what it’s going to ‘see’ next, and thus, in order to stay in sync with the world, all we need to do is adjust our models based on the error between our top-down and lateral predictions and the upward flow of sensory input: that is, our surprise.</p><figure name="632d" id="632d" class="graf graf--figure graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 367px; max-height: 362px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 98.6%;"></div><img class="graf-image" data-image-id="1*4Ut8mO7WMb5e0oG9BvzHkA.gif" data-width="367" data-height="362" src="https://cdn-images-1.medium.com/max/1600/1*4Ut8mO7WMb5e0oG9BvzHkA.gif"></div><figcaption class="imageCaption">Prediction error (deviation from the expected position of the circle) is shown in red. Our simplistic model learns to predict linear motion, but is ‘surprised’ by each bounce, resulting in a spike in prediction error.</figcaption></figure><h4 name="beef" id="beef" class="graf graf--h4 graf-after--figure">Putting it Together</h4><p name="e3f0" id="e3f0" class="graf graf--p graf-after--h4">So, to summarize, at any given moment in time, each region of our brain exists in a continuous loop:</p><figure name="5e34" id="5e34" class="graf graf--figure graf-after--p"><div class="aspectRatioPlaceholder is-locked" style="max-width: 700px; max-height: 648px;"><div class="aspectRatioPlaceholder-fill" style="padding-bottom: 92.60000000000001%;"></div><img class="graf-image" data-image-id="1*TnFHIjNjVoSZM1ddzePyZQ.png" data-width="756" data-height="700" src="https://cdn-images-1.medium.com/max/1600/1*TnFHIjNjVoSZM1ddzePyZQ.png"></div></figure><h4 name="8308" id="8308" class="graf graf--h4 graf-after--figure">Implications</h4><p name="2257" id="2257" class="graf graf--p graf-after--h4">When we zoom out from all of this, we can see that our brains are in essence prediction machines that strive to minimize surprise by recognizing patterns and associating them with other patterns. Since the information we receive is noisy and often extremely incomplete, we’ve adapted to aggressively fill in gaps or generalize out from a small set of perceptions. We’re not always successful, but overall we’re shockingly good at these tasks. We are constantly predicting what’s about to happen, and because our predictions are never exactly right we continuously update an ever-changing model of our ever-changing environment.</p><p name="17c9" id="17c9" class="graf graf--p graf-after--p">Most if not all of our <a href="https://en.wikipedia.org/wiki/List_of_cognitive_biases#/media/File:The_Cognitive_Bias_Codex_-_180%2B_biases,_designed_by_John_Manoogian_III_%28jm3%29.png" data-href="https://en.wikipedia.org/wiki/List_of_cognitive_biases#/media/File:The_Cognitive_Bias_Codex_-_180%2B_biases,_designed_by_John_Manoogian_III_(jm3).png" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">cognitive biases</a> flow naturally from this understanding of perception. Many such biases are not weaknesses or failures of the system evolution has developed for us to understand the world, but instances of maladaptation to the modern context.</p><p name="10af" id="10af" class="graf graf--p graf-after--p">Another surprising implication  is an intuitive reframing of a recently popular argument that we never experience raw reality. What we think of as perception is a ‘controlled hallucination’ to borrow Clark’s words, which our brains have designed to be precisely as <em class="markup--em markup--p-em">simple </em>and<em class="markup--em markup--p-em"> useful</em> to us as possible. </p><p name="2249" id="2249" class="graf graf--p graf-after--p">Events that are predicted eventually fade from our conscious experience when  they’re no  longer useful—we call this habituation. Again, our experience of the world <em class="markup--em markup--p-em">is itself </em>the downward flowing predictions and feedback generated in our model. Think about the <a href="https://www.youtube.com/watch?v=zsTDnnh7T6A" data-href="https://www.youtube.com/watch?v=zsTDnnh7T6A" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">well-known</a> experience of preparing to touch a static-y doorknob (you ‘feel’ the feared spark well before your hand contacts metal). Our brain’s model integrates and predicts across all of our senses, which is why we can close our eyes and continue walking a surprisingly long distance without tripping (our model of the road is good enough for quite a while).  </p><p name="98ac" id="98ac" class="graf graf--p graf-after--p graf--trailing">Regardless of whether the <a href="https://www.theguardian.com/technology/2016/oct/11/simulated-world-elon-musk-the-matrix" data-href="https://www.theguardian.com/technology/2016/oct/11/simulated-world-elon-musk-the-matrix" class="markup--anchor markup--p-anchor" rel="noopener" target="_blank">prophets</a> are right, we are most certainly living in a simulation — one that evolved over a few hundred million years, and which we’ve been updating continuously since the day we were born.</p></div></div></section><section name="db4b" class="section section--body section--last"><div class="section-divider"><hr class="section-divider"></div><div class="section-content"><div class="section-inner sectionLayout--insetColumn"><h4 name="817d" id="817d" class="graf graf--h4 graf--leading">Other things to read</h4><ul class="postList"><li name="6191" id="6191" class="graf graf--li graf-after--h4"><a href="https://www.goodreads.com/book/show/25823558-surfing-uncertainty" data-href="https://www.goodreads.com/book/show/25823558-surfing-uncertainty" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">Surfing Uncertainty</a>, Andy Clark (2015).</li><li name="7512" id="7512" class="graf graf--li graf-after--li"><a href="https://www.goodreads.com/book/show/27539.On_Intelligence" data-href="https://www.goodreads.com/book/show/27539.On_Intelligence" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">On Intelligence</a>, Jeff Hawkins (2005).</li><li name="04d4" id="04d4" class="graf graf--li graf-after--li"><a href="https://www.goodreads.com/book/show/2069.Consciousness_Explained" data-href="https://www.goodreads.com/book/show/2069.Consciousness_Explained" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">Consciousness Explained</a>, Daniel Dennett (1992). Dennett introduces his multiple drafts model which is full of parallels with the theories above.</li><li name="11e1" id="11e1" class="graf graf--li graf-after--li"><a href="http://numenta.com/papers/" data-href="http://numenta.com/papers/" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">Numenta white papers</a>, papers from Numenta’s research, and implementations of learning algorithms for spatial pooling and sequence learning (temporal memory).</li><li name="c6ff" id="c6ff" class="graf graf--li graf-after--li">Lots of great short pieces from Mark Humphries at <a href="https://medium.com/the-spike" data-href="https://medium.com/the-spike" class="markup--anchor markup--li-anchor" target="_blank">The Spike</a>.</li><li name="bea5" id="bea5" class="graf graf--li graf-after--li"><a href="https://arxiv.org/abs/1512.05245" data-href="https://arxiv.org/abs/1512.05245" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">Symphony from Synapses: Neocortex as a Universal Dynamical Systems Modeller using Hierarchical Temporal Memory</a>, Fergal Byrne (2015).</li><li name="7002" id="7002" class="graf graf--li graf-after--li"><a href="https://www.wired.com/2017/02/life-death-spring-disorder/" data-href="https://www.wired.com/2017/02/life-death-spring-disorder/" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">How Life (and Death) Spring from Disorder</a>, Wired (2017), on a thermodynamic process that all of this brain world-model building may, incredibly, be a subset of.</li></ul><h4 name="45a3" id="45a3" class="graf graf--h4 graf-after--li">Other resources</h4><ul class="postList"><li name="1284" id="1284" class="graf graf--li graf-after--h4"><a href="http://neuroscience.uth.tmc.edu/" data-href="http://neuroscience.uth.tmc.edu/" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">UTHealth’s neuroscience lectures</a> are all online and totally free, which is incredible. I’m still working on this, as the level of detail goes quite deep, but as a reference for those interested in the biology, it’s invaluable. </li><li name="f714" id="f714" class="graf graf--li graf-after--li"><a href="https://www.coursera.org/learn/computational-neuroscience/" data-href="https://www.coursera.org/learn/computational-neuroscience/" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">Computational Neuroscience</a> (Coursera, UW). I can recommend this course to anyone new to computational neuroscience, and not too afraid of differential equations.</li><li name="51f0" id="51f0" class="graf graf--li graf-after--li"><a href="https://www.youtube.com/playlist?list=PL3yXMgtrZmDqhsFQzwUC9V8MeeVOQ7eZ9" data-href="https://www.youtube.com/playlist?list=PL3yXMgtrZmDqhsFQzwUC9V8MeeVOQ7eZ9" class="markup--anchor markup--li-anchor" rel="noopener" target="_blank">HTM School</a>, Numenta’s series on learning NuPIC, an open source implementation of Hierarchical Temporal Memory</li></ul><p name="85bb" id="85bb" class="graf graf--p graf--empty graf-after--li graf--trailing"><br></p></div></div></section>
</section>