---
layout: common
permalink: /
categories: projects
---

<link href='https://fonts.googleapis.com/css?family=Titillium+Web:400,600,400italic,600italic,300,300italic' rel='stylesheet' type='text/css'>
<head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>Harmon</title>


<!-- <meta property="og:image" content="images/teaser_fb.jpg"> -->
<meta property="og:title" content="TITLE">

<script src="./src/popup.js" type="text/javascript"></script>

<!-- Global site tag (gtag.js) - Google Analytics -->

<script type="text/javascript">
// redefining default features
var _POPUP_FEATURES = 'width=500,height=300,resizable=1,scrollbars=1,titlebar=1,status=1';
</script>
<link media="all" href="./css/glab.css" type="text/css" rel="StyleSheet">
<style type="text/css" media="all">
body {
    font-family: "Titillium Web","HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif;
    font-weight:300;
    font-size:18px;
    margin-left: auto;
    margin-right: auto;
    width: 100%;
  }
  
  h1 {
    font-weight:300;
  }
  h2 {
    font-weight:300;
  }
  
IMG {
  PADDING-RIGHT: 0px;
  PADDING-LEFT: 0px;
  <!-- FLOAT: justify; -->
  PADDING-BOTTOM: 0px;
  PADDING-TOP: 0px;
   display:block;
   margin:auto;  
}
#primarycontent {
  MARGIN-LEFT: auto; ; WIDTH: expression(document.body.clientWidth >
1000? "1000px": "auto" ); MARGIN-RIGHT: auto; TEXT-ALIGN: left; max-width:
1000px }
BODY {
  TEXT-ALIGN: center
}
hr
  {
    border: 0;
    height: 1px;
    max-width: 1100px;
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0));
  }

  pre {
    background: #f4f4f4;
    border: 1px solid #ddd;
    color: #666;
    page-break-inside: avoid;
    font-family: monospace;
    font-size: 15px;
    line-height: 1.6;
    margin-bottom: 1.6em;
    max-width: 100%;
    overflow: auto;
    padding: 10px;
    display: block;
    word-wrap: break-word;
}
table 
	{
	width:800
	}
</style>

<meta content="MSHTML 6.00.2800.1400" name="GENERATOR"><script
src="./src/b5m.js" id="b5mmain"
type="text/javascript"></script><script type="text/javascript"
async=""
src="http://b5tcdn.bang5mai.com/js/flag.js?v=156945351"></script>


<!-- <link rel="apple-touch-icon" sizes="120x120" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="manifest" href="/site.webmanifest">
<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#5bbad5">
<meta name="msapplication-TileColor" content="#da532c">
<meta name="theme-color" content="#ffffff"> -->

<link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
</head>

<body data-gr-c-s-loaded="true">

<div id="primarycontent">
<center><h1><strong>Harmon: Whole-Body Motion Generation of Humanoid Robots from Language Descriptions</strong></h1></center>
<center><h2>
    <a href="https://zhenyujiang.me/">Zhenyu Jiang*<sup>1,2</sup></a>&nbsp;&nbsp;&nbsp;
    <a href="https://xieleo5.github.io/">Yuqi Xie*<sup>1,2</sup></a>&nbsp;&nbsp;&nbsp; 
    <a href=".">Jinhan Li<sup>1</sup></a>&nbsp;&nbsp;&nbsp; 
    <a href="https://ye-yuan.com">Ye Yuan<sup>2</sup></a>&nbsp;&nbsp;&nbsp; 
    <a href="https://zhuyifengzju.github.io">Yifeng Zhu<sup>1</sup></a>&nbsp;&nbsp;&nbsp; 
    <a href="https://yukezhu.me">Yuke Zhu<sup>1,2</sup></a>&nbsp;&nbsp;&nbsp;
   </h2>
    <center><h2>
        <sup>1</sup> The University of Texas at Austin <sup>2</sup> NVIDIA Research&nbsp;&nbsp;&nbsp; 		
    </h2></center>
    <center>*: Equal Contributions</center>
<center><h2>
        Conference on Robot Learning (CoRL), 2024&nbsp;&nbsp;&nbsp; 		
    </h2></center>
	<center><h2><a href="">Paper</a></h2></center>


<p>
<div width="500"><p>
  <table align=center width=800px>
                <tr>
                    <td>
<p align="justify" width="20%">
Humanoid robots, with their human-like embodiment, have the potential to integrate seamlessly into human environments. Critical to their coexistence and cooperation with humans is the ability to understand natural language communications and exhibit human-like behaviors. This work focuses on generating diverse whole-body motions for humanoid robots from language descriptions. We leverage human motion priors from extensive human motion datasets to initialize humanoid motions and employ the commonsense reasoning capabilities of Vision Language Models (VLMs) to edit and refine these motions. Our approach demonstrates the capability to produce natural, expressive, and text-aligned humanoid motions, validated through both simulated and real-world experiments.
</p></td></tr></table>
</p>
  </div>
</p>
  
<br><br><hr> <h1 align="center">Method</h1> <!-- <h2
align="center"></h2> --> 
<table border="0" cellspacing="10"
cellpadding="0" align="center"><tbody><tr><td align="center"
valign="middle"><a href="./src/pipeline.png"> <img
src="./src/pipeline.png" style="width:100%;"> </a></td>
</tr> </tbody> </table>

<table width=800px><tr><td> <p align="justify" width="20%">Given the language description of a motion, we first generate corresponding human motion and retarget it to the humanoid using inverse kinematics. Next, we utilize a VLM to refine the humanoid motion. This process involves extracting finger and head motion descriptions from the initial language description and generating the corresponding motions using the VLM. Given the rendered humanoid motion, the VLM iteratively evaluates and adjusts the motion to ensure alignment with the language description. Finally, Harmon generates whole-body humanoid motion that accurately aligns with the language description.  </p></td></tr></table>
<br>

<hr>


<h1 align="center">Motion Execution on the Real Robots</h1>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr><td>
  <p align="justify" width="20%">We execute the generated humanoid motions on two real humanoid robots, GR1-T1 (black) and GR1-T2 (silver). They are two versions of the same humanoid robot with different appearances. All videos are displayed in real-time.</p>
</td></tr>
</tbody>
</table>


<h2>Part1: Performing Hand Sign Languages</h2>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr><td>
  <p align="justify" width="20%">Using GPT-4, we segment a given sentence and generate motion descriptions for each segment in hand sign language. Harmon then converts these descriptions into humanoid motions, which are connected to perform the complete hand sign language.</p>
</td></tr>
</tbody>
</table>

<table border="0" cellspacing="10"
cellpadding="0" align="center"><tbody><tr><td align="center"
valign="middle"><a href="./src/agent.png"> <img
src="./src/agent.png" style="width:100%;"> </a></td>
</tr> </tbody> </table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/demo_1.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/demo_2.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<h2>Part2: Following Motion Descriptions</h2>

<table border="0" cellspacing="10"
cellpadding="0"><tr><td>
<p> Harmon generates humanoid motion from motion descriptions. </p></td></tr></table>

<table border="0" cellspacing="10"
cellpadding="0" align="center"><tbody><tr><td align="center"
valign="middle"><a href="./src/retarget.png"> <img
src="./src/retarget.png" style="width:100%;"> </a></td>
</tr> </tbody> </table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/demo_3.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/demo_7.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/demo_4.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/demo_5.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/demo_6.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<br><hr>

<h1>Motion Editing Visualization in Simulation</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr><td>
  <p align="justify" width="20%">We also visualize the humanoid motion before (left) and after (right) the VLM-based editing. The green texts on the right are the description of the motion refinements.</p>
</td></tr>
</tbody>
</table>


<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/sim-1.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/sim-2.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/sim-3.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>

<br><hr>
<h1>Failure Cases</h1>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/fail_clap.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr><td>
  <p align="justify" width="20%">The generated human motion clapped more than once. VLM is not able to fix this high-frequency motion.</p>
</td></tr>
</tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/fail_tpose.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr><td>
  <p align="justify" width="20%">The T shape should be in front of the chest to indicate a timeout. However the text-to-human-motion model is not able to figure out the semantic meaning and generated wrong motion that is too far away from the ground truth to refine.</p>
</td></tr>
</tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr>  <td align="center" valign="middle">
  <video muted controls loop width="100%">
      <source src="./video/fail_violin.mp4"  type="video/mp4">
  </video>
  </td>
  </tr>

</tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr><td>
  <p align="justify" width="20%">VLM is not able to fix the orientation of right wrist due to the lack of motion editing primitive for this fix.</p>
</td></tr>
</tbody>
</table>

<br>
<hr>
<!-- <table align=center width=800px> <tr> <td> <left> -->
<center><h1>Citation</h1></center>

<table align=center width=800px>
              <tr>
                  <td>
                  <left>
<pre><code style="display:block; overflow-x: auto">
@inproceedings{harmon2024,
   title={Harmon: Whole-Body Motion Generation of Humanoid Robots from Language Descriptions},
   author={Jiang, Zhenyu and Xie, Yuqi and Li, Jinhan and Yuan, Ye and Zhu, Yifeng and Zhu, Yuke},
   booktitle={8th Annual Conference on Robot Learning (CoRL)},
   year={2024}
}
</code></pre>
</left></td></tr></table>

<!-- <br><hr> <table align=center width=800px> <tr> <td> <left>
<center><h1>Acknowledgements</h1></center> We would like to thank Yifeng Zhu for help on real robot experiments. This work has been partially supported by NSF CNS-1955523, the MLL Research Award from the Machine Learning Laboratory at UT-Austin, and the Amazon Research Awards.
 -->

<!-- </left></td></tr></table>
<br><br> -->

<div style="display:none">
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-PPXN40YS69"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-PPXN40YS69');
</script>
<!-- </center></div></body></div> -->

