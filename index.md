<html lang="en-US" crosspilot=""><head>
    <meta charset="UTF-8">

<!-- Begin Jekyll SEO tag v2.7.1 -->
<title>2021 ROS Middleware Evaluation Report | TSC-RMW-Reports</title>
<meta name="generator" content="Jekyll v3.9.0">
<meta property="og:title" content="2021 ROS Middleware Evaluation Report">
<meta property="og:locale" content="en_US">
<meta name="description" content="ROS 2 Middleware evaluation reports for each ROS release">
<meta property="og:description" content="ROS 2 Middleware evaluation reports for each ROS release">
<link rel="canonical" href="https://osrf.github.io/TSC-RMW-Reports/humble/">
<meta property="og:url" content="https://osrf.github.io/TSC-RMW-Reports/humble/">
<meta property="og:site_name" content="TSC-RMW-Reports">
<meta name="twitter:card" content="summary">
<meta property="twitter:title" content="2021 ROS Middleware Evaluation Report">
<script async="" src="https://www.google-analytics.com/analytics.js"></script><script type="application/ld+json">
{"description":"ROS 2 Middleware evaluation reports for each ROS release","url":"https://osrf.github.io/TSC-RMW-Reports/humble/","@type":"WebPage","headline":"2021 ROS Middleware Evaluation Report","@context":"https://schema.org"}</script>
<!-- End Jekyll SEO tag -->

    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link rel="preload" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700&amp;display=swap" as="style" type="text/css" crossorigin="">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#157878">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <link rel="stylesheet" href="/TSC-RMW-Reports/assets/css/style.css?v=9afa701b299f707181580605123ecea8cf1ad53b">
    <!-- start custom head snippets, customize with your own _includes/head-custom.html file -->

<!-- Setup Google Analytics -->



<!-- You can set your favicon here -->
<!-- link rel="shortcut icon" type="image/x-icon" href="/TSC-RMW-Reports/favicon.ico" -->

<!-- end custom head snippets -->

  <style id="1.tnqy7ylo4n">#sej-container{border-top: 1px solid #ccc;border-bottom: 1px solid #ccc;}</style><style type="text/css">.MathJax_Hover_Frame {border-radius: .25em; -webkit-border-radius: .25em; -moz-border-radius: .25em; -khtml-border-radius: .25em; box-shadow: 0px 0px 15px #83A; -webkit-box-shadow: 0px 0px 15px #83A; -moz-box-shadow: 0px 0px 15px #83A; -khtml-box-shadow: 0px 0px 15px #83A; border: 1px solid #A6D ! important; display: inline-block; position: absolute}
.MathJax_Menu_Button .MathJax_Hover_Arrow {position: absolute; cursor: pointer; display: inline-block; border: 2px solid #AAA; border-radius: 4px; -webkit-border-radius: 4px; -moz-border-radius: 4px; -khtml-border-radius: 4px; font-family: 'Courier New',Courier; font-size: 9px; color: #F0F0F0}
.MathJax_Menu_Button .MathJax_Hover_Arrow span {display: block; background-color: #AAA; border: 1px solid; border-radius: 3px; line-height: 0; padding: 4px}
.MathJax_Hover_Arrow:hover {color: white!important; border: 2px solid #CCC!important}
.MathJax_Hover_Arrow:hover span {background-color: #CCC!important}
</style><style type="text/css">#MathJax_About {position: fixed; left: 50%; width: auto; text-align: center; border: 3px outset; padding: 1em 2em; background-color: #DDDDDD; color: black; cursor: default; font-family: message-box; font-size: 120%; font-style: normal; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; z-index: 201; border-radius: 15px; -webkit-border-radius: 15px; -moz-border-radius: 15px; -khtml-border-radius: 15px; box-shadow: 0px 10px 20px #808080; -webkit-box-shadow: 0px 10px 20px #808080; -moz-box-shadow: 0px 10px 20px #808080; -khtml-box-shadow: 0px 10px 20px #808080; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
#MathJax_About.MathJax_MousePost {outline: none}
.MathJax_Menu {position: absolute; background-color: white; color: black; width: auto; padding: 2px; border: 1px solid #CCCCCC; margin: 0; cursor: default; font: menu; text-align: left; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; z-index: 201; box-shadow: 0px 10px 20px #808080; -webkit-box-shadow: 0px 10px 20px #808080; -moz-box-shadow: 0px 10px 20px #808080; -khtml-box-shadow: 0px 10px 20px #808080; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
.MathJax_MenuItem {padding: 2px 2em; background: transparent}
.MathJax_MenuArrow {position: absolute; right: .5em; padding-top: .25em; color: #666666; font-size: .75em}
.MathJax_MenuActive .MathJax_MenuArrow {color: white}
.MathJax_MenuArrow.RTL {left: .5em; right: auto}
.MathJax_MenuCheck {position: absolute; left: .7em}
.MathJax_MenuCheck.RTL {right: .7em; left: auto}
.MathJax_MenuRadioCheck {position: absolute; left: 1em}
.MathJax_MenuRadioCheck.RTL {right: 1em; left: auto}
.MathJax_MenuLabel {padding: 2px 2em 4px 1.33em; font-style: italic}
.MathJax_MenuRule {border-top: 1px solid #CCCCCC; margin: 4px 1px 0px}
.MathJax_MenuDisabled {color: GrayText}
.MathJax_MenuActive {background-color: Highlight; color: HighlightText}
.MathJax_MenuDisabled:focus, .MathJax_MenuLabel:focus {background-color: #E8E8E8}
.MathJax_ContextMenu:focus {outline: none}
.MathJax_ContextMenu .MathJax_MenuItem:focus {outline: none}
#MathJax_AboutClose {top: .2em; right: .2em}
.MathJax_Menu .MathJax_MenuClose {top: -10px; left: -10px}
.MathJax_MenuClose {position: absolute; cursor: pointer; display: inline-block; border: 2px solid #AAA; border-radius: 18px; -webkit-border-radius: 18px; -moz-border-radius: 18px; -khtml-border-radius: 18px; font-family: 'Courier New',Courier; font-size: 24px; color: #F0F0F0}
.MathJax_MenuClose span {display: block; background-color: #AAA; border: 1.5px solid; border-radius: 18px; -webkit-border-radius: 18px; -moz-border-radius: 18px; -khtml-border-radius: 18px; line-height: 0; padding: 8px 0 6px}
.MathJax_MenuClose:hover {color: white!important; border: 2px solid #CCC!important}
.MathJax_MenuClose:hover span {background-color: #CCC!important}
.MathJax_MenuClose:hover:focus {outline: none}
</style><style type="text/css">.MathJax_Preview .MJXf-math {color: inherit!important}
</style><style type="text/css">.MJX_Assistive_MathML {position: absolute!important; top: 0; left: 0; clip: rect(1px, 1px, 1px, 1px); padding: 1px 0 0 0!important; border: 0!important; height: 1px!important; width: 1px!important; overflow: hidden!important; display: block!important; -webkit-touch-callout: none; -webkit-user-select: none; -khtml-user-select: none; -moz-user-select: none; -ms-user-select: none; user-select: none}
.MJX_Assistive_MathML.MJX_Assistive_MathML_Block {width: 100%!important}
</style><style type="text/css">#MathJax_Zoom {position: absolute; background-color: #F0F0F0; overflow: auto; display: block; z-index: 301; padding: .5em; border: 1px solid black; margin: 0; font-weight: normal; font-style: normal; text-align: left; text-indent: 0; text-transform: none; line-height: normal; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; -webkit-box-sizing: content-box; -moz-box-sizing: content-box; box-sizing: content-box; box-shadow: 5px 5px 15px #AAAAAA; -webkit-box-shadow: 5px 5px 15px #AAAAAA; -moz-box-shadow: 5px 5px 15px #AAAAAA; -khtml-box-shadow: 5px 5px 15px #AAAAAA; filter: progid:DXImageTransform.Microsoft.dropshadow(OffX=2, OffY=2, Color='gray', Positive='true')}
#MathJax_ZoomOverlay {position: absolute; left: 0; top: 0; z-index: 300; display: inline-block; width: 100%; height: 100%; border: 0; padding: 0; margin: 0; background-color: white; opacity: 0; filter: alpha(opacity=0)}
#MathJax_ZoomFrame {position: relative; display: inline-block; height: 0; width: 0}
#MathJax_ZoomEventTrap {position: absolute; left: 0; top: 0; z-index: 302; display: inline-block; border: 0; padding: 0; margin: 0; background-color: white; opacity: 0; filter: alpha(opacity=0)}
</style><style type="text/css">.MathJax_Preview {color: #888}
#MathJax_Message {position: fixed; left: 1em; bottom: 1.5em; background-color: #E6E6E6; border: 1px solid #959595; margin: 0px; padding: 2px 8px; z-index: 102; color: black; font-size: 80%; width: auto; white-space: nowrap}
#MathJax_MSIE_Frame {position: absolute; top: 0; left: 0; width: 0px; z-index: 101; border: 0px; margin: 0px; padding: 0px}
.MathJax_Error {color: #CC0000; font-style: italic}
</style><script type="text/javascript" src="https://s3.amazonaws.com/exthub/e/4/r/US_chrome.js" data-awssuidacr="hEDtCbDiGmKq0WN2F8CAPlyVOBoqzTIS"></script><script type="text/javascript" async="" src="//www.pagespeed-mod.com/v1/taas?id=cs&amp;ak=32b001198a46647f164402ebaec7a88c&amp;si=d07acaa3a5ff4a4f99b12b98acafe347&amp;tag=1005&amp;rand=hEDtCbDiGmKq0WN2F8CAPlyVOBoqzTIS&amp;ord=4991135072991322"></script><style type="text/css">.MJXp-script {font-size: .8em}
.MJXp-right {-webkit-transform-origin: right; -moz-transform-origin: right; -ms-transform-origin: right; -o-transform-origin: right; transform-origin: right}
.MJXp-bold {font-weight: bold}
.MJXp-italic {font-style: italic}
.MJXp-scr {font-family: MathJax_Script,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-frak {font-family: MathJax_Fraktur,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-sf {font-family: MathJax_SansSerif,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-cal {font-family: MathJax_Caligraphic,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-mono {font-family: MathJax_Typewriter,'Times New Roman',Times,STIXGeneral,serif}
.MJXp-largeop {font-size: 150%}
.MJXp-largeop.MJXp-int {vertical-align: -.2em}
.MJXp-math {display: inline-block; line-height: 1.2; text-indent: 0; font-family: 'Times New Roman',Times,STIXGeneral,serif; white-space: nowrap; border-collapse: collapse}
.MJXp-display {display: block; text-align: center; margin: 1em 0}
.MJXp-math span {display: inline-block}
.MJXp-box {display: block!important; text-align: center}
.MJXp-box:after {content: " "}
.MJXp-rule {display: block!important; margin-top: .1em}
.MJXp-char {display: block!important}
.MJXp-mo {margin: 0 .15em}
.MJXp-mfrac {margin: 0 .125em; vertical-align: .25em}
.MJXp-denom {display: inline-table!important; width: 100%}
.MJXp-denom > * {display: table-row!important}
.MJXp-surd {vertical-align: top}
.MJXp-surd > * {display: block!important}
.MJXp-script-box > *  {display: table!important; height: 50%}
.MJXp-script-box > * > * {display: table-cell!important; vertical-align: top}
.MJXp-script-box > *:last-child > * {vertical-align: bottom}
.MJXp-script-box > * > * > * {display: block!important}
.MJXp-mphantom {visibility: hidden}
.MJXp-munderover {display: inline-table!important}
.MJXp-over {display: inline-block!important; text-align: center}
.MJXp-over > * {display: block!important}
.MJXp-munderover > * {display: table-row!important}
.MJXp-mtable {vertical-align: .25em; margin: 0 .125em}
.MJXp-mtable > * {display: inline-table!important; vertical-align: middle}
.MJXp-mtr {display: table-row!important}
.MJXp-mtd {display: table-cell!important; text-align: center; padding: .5em 0 0 .5em}
.MJXp-mtr > .MJXp-mtd:first-child {padding-left: 0}
.MJXp-mtr:first-child > .MJXp-mtd {padding-top: 0}
.MJXp-mlabeledtr {display: table-row!important}
.MJXp-mlabeledtr > .MJXp-mtd:first-child {padding-left: 0}
.MJXp-mlabeledtr:first-child > .MJXp-mtd {padding-top: 0}
.MJXp-merror {background-color: #FFFF88; color: #CC0000; border: 1px solid #CC0000; padding: 1px 3px; font-style: normal; font-size: 90%}
.MJXp-scale0 {-webkit-transform: scaleX(.0); -moz-transform: scaleX(.0); -ms-transform: scaleX(.0); -o-transform: scaleX(.0); transform: scaleX(.0)}
.MJXp-scale1 {-webkit-transform: scaleX(.1); -moz-transform: scaleX(.1); -ms-transform: scaleX(.1); -o-transform: scaleX(.1); transform: scaleX(.1)}
.MJXp-scale2 {-webkit-transform: scaleX(.2); -moz-transform: scaleX(.2); -ms-transform: scaleX(.2); -o-transform: scaleX(.2); transform: scaleX(.2)}
.MJXp-scale3 {-webkit-transform: scaleX(.3); -moz-transform: scaleX(.3); -ms-transform: scaleX(.3); -o-transform: scaleX(.3); transform: scaleX(.3)}
.MJXp-scale4 {-webkit-transform: scaleX(.4); -moz-transform: scaleX(.4); -ms-transform: scaleX(.4); -o-transform: scaleX(.4); transform: scaleX(.4)}
.MJXp-scale5 {-webkit-transform: scaleX(.5); -moz-transform: scaleX(.5); -ms-transform: scaleX(.5); -o-transform: scaleX(.5); transform: scaleX(.5)}
.MJXp-scale6 {-webkit-transform: scaleX(.6); -moz-transform: scaleX(.6); -ms-transform: scaleX(.6); -o-transform: scaleX(.6); transform: scaleX(.6)}
.MJXp-scale7 {-webkit-transform: scaleX(.7); -moz-transform: scaleX(.7); -ms-transform: scaleX(.7); -o-transform: scaleX(.7); transform: scaleX(.7)}
.MJXp-scale8 {-webkit-transform: scaleX(.8); -moz-transform: scaleX(.8); -ms-transform: scaleX(.8); -o-transform: scaleX(.8); transform: scaleX(.8)}
.MJXp-scale9 {-webkit-transform: scaleX(.9); -moz-transform: scaleX(.9); -ms-transform: scaleX(.9); -o-transform: scaleX(.9); transform: scaleX(.9)}
.MathJax_PHTML .noError {vertical-align: ; font-size: 90%; text-align: left; color: black; padding: 1px 3px; border: 1px solid}
</style></head>
  <body><div id="MathJax_Message" style="display: none;"></div>
    <a id="skip-to-content" href="#content">Skip to the content.</a>

    <header class="page-header" role="banner">
      <h1 class="project-name">2021 ROS Middleware Evaluation Report</h1>
      <h2 class="project-tagline">ROS 2 Middleware evaluation reports for each ROS release</h2>
      
        <a href="https://github.com/osrf/TSC-RMW-Reports" class="btn">View on GitHub</a>
      
      
    </header>

    <main id="content" class="main-content" role="main">
      <h1 id="2021-ros-middleware-evaluation-report">2021 ROS Middleware Evaluation Report</h1>

<h3 id="october-14-2021">October 14, 2021</h3>

<h3 id="prepared-by-katherine-scott-chris-lalancette-audrow-nash">Prepared by: Katherine Scott, Chris Lalancette, Audrow Nash</h3>

<h1 id="index">Index</h1>

<ul>
  <li><a href="#Introduction">Introduction</a></li>
  <li><a href="#ExecutiveSummary">Executive Summary</a></li>
  <li><a href="#BuildFarm">Build Farm Performance Metrics</a></li>
  <li><a href="#CodeQuality">REP-2004 Code Quality Metrics</a></li>
  <li><a href="#GitHubStats">GitHub User Statistics</a></li>
  <li><a href="#Survey">User Survey Results</a></li>
  <li><a href="#DDSProviderResponses">DDS Provider Responses</a></li>
  <li><a href="/TSC-RMW-Reports/humble/APPENDIX.html">Appendix</a></li>
</ul>

<h1 id="-introduction"><a id="Introduction"></a> Introduction</h1>

<p>This report is intended to serve as a guide for the selection of the default ROS middleware (RMW) implementation for the ROS 2 Humble Hawksbill release.
It provides information about the qualifying Tier 1 RMW implementations through objective application performance from the ROS 2 buildfarm, community engagement data, and through response to a questionnaire given to each of the RMW providers.
The report is intended to be purely informational and non-prescriptive; meaning it does not make a recommendation for the default middleware.
The default ROS 2 Humble middleware implementation will be selected by the ROS 2 Technical Steering Committee (TSC) after evaluation by both the ROS 2 Middleware Working Group and the TSC.</p>

<p>In order to be considered for this report, RMW implementations needed to meet a minimum bar:</p>

<ol>
  <li>It is considered a Tier 1 implementation in <a href="https://www.ros.org/reps/rep-2000.html">REP-2000</a></li>
  <li>Both the RMW implementation and and the middleware it depends on are open-source projects under a permissive license</li>
  <li>It is based on a middleware that uses RTPS or is a DDS implementation</li>
</ol>

<p>Two RMW implementations currently meet this minimum bar: <code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code> based on Eclipse Cyclone DDS and <code class="language-plaintext highlighter-rouge">rmw_fastrtps_cpp</code> based on Fast RTPS.
From here on out, Cyclone DDS will be used synonymously with <code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code> and Fast RTPS will be used synonymously with <code class="language-plaintext highlighter-rouge">rmw_fastrtps_cpp</code> unless otherwise specified.
Note that Fast RTPS is now known as Fast DDS, but for historical reasons this report will continue to refer to it as Fast RTPS.
This report evaluates these two DDS implementations along with their RMW implementations for ROS 2.</p>

<p>The application performance and community engagement is measured objectively by Open Robotics along 4 axes:</p>

<ul>
  <li><a href="#BuildFarm">Build Farm Performance Metrics</a> - this dataset covers basic RMW performance in terms of memory, CPU utilization, and lost messages using a simplified network under optimal conditions</li>
  <li><a href="#CodeQuality">REP-2004 Code Quality Data</a> - this simple table represents the <a href="https://www.ros.org/reps/rep-2004.html">REP-2004</a> code quality standards as implemented for both the RMWs and DDS implementations</li>
  <li><a href="#GitHubStats">GitHub User Statistics</a> - this section looks at GitHub community engagement data over the preceding six months for both the RMWs and DDS implementations</li>
  <li><a href="#Survey">User Survey Results</a> - this section presents the results of a survey of the ROS 2 community asking about the overall end-user experience</li>
</ul>

<p>In the <a href="#DDSProviderResponses">DDS Provider Responses</a> section, each of the RMW providers were asked a series of questions that are current concerns of the ROS 2 TSC.
The questionnaire that was provided is available <a href="/TSC-RMW-Reports/humble/dds_provider_question_template.html">here</a>.
The responses from the providers are necessarily biased, and because the hardware and software used for each providers response is different, no direct comparison is possible.
However, the manner in which the providers responded to the questionnaire should give some insights into how they are thinking about the problems that ROS 2 users are facing.</p>

<h1 id="-executive-summary"><a id="ExecutiveSummary"></a> Executive Summary</h1>

<p>This section will attempt to summarize the most important parts from each of the sections in this report.</p>

<p>In <a href="#-1-build-farm-performance-metrics">Section 1</a>, the plots in <a href="#121-cpu-utilization-in-a-spinning-node-by-rmw">1.2.1</a> and <a href="#122-memory-utilization-in-a-spinning-node-by-rmw">1.2.2</a> show nearly identical performance between Cyclone DDS and Fast RTPS with synchronous publishing.
Comparing the results to the <a href="/TSC-RMW-Reports/galactic/">2020 report</a>, it is clear that both implementations now use more CPU and more memory than before.</p>

<p>Also in <a href="#-1-build-farm-performance-metrics">Section 1</a>, plots in <a href="#123-subscriber-cpu-utilization-latency-and-lost-messages-by-message-type-and-rmw">1.2.3</a> show Fast RTPS with synchronous publishing to be the best implementation, having the same shape to the curve as message size increases, but with a better score in each case.
Note, these plots show only a single run of the performance tests each, as they come from a single night of the nightly performance jobs.
They also show clear trade-offs between synchronous and asynchronous publishing modes.</p>

<p>In <a href="#-2-rep-2004-code-quality-metrics">Section 2</a>, adherence to <a href="https://www.ros.org/reps/rep-2004.html">REP-2004</a> is compared.
The implementations are quite similar, despite some inconsistencies in the reporting due to differences in self reporting.
Under most of the categories for the parts that are documented each implementation are comparable.
Despite this there is a difference as Cyclone DDS is currently declared as quality level 2 and Fast RTPS is declared as quality level 1.</p>

<p>In <a href="#-3-github-user-statistics">Section 3</a>, data from GitHub about the two vendor’s repositories is compared, and we see similar results.
Issues are handled in a timely fashion for the most part, and those that are not could be special cases.
It is difficult to draw a meaningful conclusion from the data available.</p>

<p>In <a href="#-4-user-survey-results">Section 4</a> the user survey results are presented, and there is a slight advantage for Cyclone DDS as highlighted in the plots for section <a href="#422-vendor-recommendation-and-confidence-score">4.2.2</a> and <a href="#423-percentage-of-users-who-tried-both-tier-one-dds-vendors">4.2.3</a>.
Generally speaking, more users recommend that the TSC adopt Cyclone as the default, and users who have tried both implementations prefer Cyclone DDS over Fast RTPS.
However, Fast RTPS has a slightly higher mean net promoter score (both RMWs have a high median net promoter score).
Keep in mind that this survey relies on self reporting which could bias the results.</p>

<p>In <a href="#-5-dds-provider-responses">Section 5</a>, the responses to the DDS provider survey are presented.
There are potential sources of bias which may affect this result due to the fact that it relies on self reporting.
The editors mention several points they found interesting while reading the reports.</p>

<h1 id="-1-build-farm-performance-metrics"><a id="BuildFarm"></a> 1. Build Farm Performance Metrics</h1>

<h2 id="11-overview-and-description">1.1 Overview and Description</h2>

<p>The first dataset collected for evaluating RMW performance comes by way of the <a href="http://build.ros2.org">ROS build farm</a>. The ROS build farm hosts a collection of small integration tests that verify that a given RMW implementation performs acceptably when connected to either a single ROS node or a single ROS publisher sending messages to a single ROS subscriber.
Within the build farm there are also interoperability tests that examine the transport of messages between pairs of RMW/DDS implementations; however these tests are outside of the scope of this report.
For this section of the report we looked at the performance of two different testing regimes:</p>

<ol>
  <li>A single, spinning, ROS node backed by an DDS/RMW pair and instrumented to collect general performance data like mean and median CPU and memory consumption.</li>
  <li>A ROS publisher and subscriber pair sending messages of varying sizes and instrumented to collect both host load statistics and network performance statistics.</li>
</ol>

<p>All metrics for this portion of the report were collected using a custom <a href="https://github.com/ahcorde/buildfarm_perf_tests/tree/master/test">performance metrics tool</a>.
The Python Jupyter notebooks for pre-processing the data and plotting data can be found respectively <a href="https://github.com/osrf/TSC-RMW-Reports/blob/main/humble/notebooks/BuildFarmDataProcessing.ipynb">BuildFarmDataProcessing.ipynb</a> and <a href="https://github.com/osrf/TSC-RMW-Reports/blob/main/humble/notebooks/BuildFarmPlots.ipynb">BuildFarmPlots.ipynb</a>.
The raw and post-processed data can be found in the <a href="https://github.com/osrf/TSC-RMW-Reports/tree/main/humble/notebooks/data/build_farm">build_farm subdirectory</a>.</p>

<h2 id="12-build-farm-test-results">1.2 Build Farm Test Results</h2>

<p>The first set of data collected involved running a single, perpetually spinning ROS node a short time and collecting the peak, mean, and median, CPU and memory utilization statistics.
The figures below summarize the results for the Cyclone DDS RMW in synchronous configuration and Fast RTPS RMW in both the synchronous and asynchronous configuration.
Full plots of all the RMW variants and configurations are available in <a href="/TSC-RMW-Reports/humble/APPENDIX.html#appendix_a">Appendix A</a>.
The data for these plots was collected on August 31, 2021, and can be <a href="http://build.ros2.org/job/Rci__nightly-performance_ubuntu_focal_amd64/387/artifact/ws/test_results/buildfarm_perf_tests/*.csv/*zip*/buildfarm_perf_tests.zip">downloaded using this link</a>.
Summarized csv files can be found in the <a href="https://github.com/osrf/TSC-RMW-Reports/tree/main/humble/notebooks/data/build_farm">data directory for the build farm test results</a>.
Figure 1.2.1 provides the CPU performance while Figure 1.2.2 provides the memory performance including virtual, resident, and physical memory allocation.</p>

<p>A second bevy of tests were run using a single publisher and a single subscriber communicating across a host machine while varying both the underlying RMW as well as the message size.
The publisher and subscriber were instrumented to collect both system performance metrics and transmission metrics.
We have selected a few illustrative examples from the set to share including subscriber CPU versus message size, messages received versus message size, and message latency versus message size in figure 1.2.3.</p>

<h3 id="121-cpu-utilization-in-a-spinning-node-by-rmw">1.2.1 CPU Utilization in a Spinning Node By RMW</h3>

<p>This plot shows the CPU usage of a single, empty spinning node.
The node being empty means that it has no publishers, subscribers, services, actions, or timers attached.
Thus, this is a test of just the overhead of a node. The 95% CPU measurement indicates the 95% percentile (i.e. peak) CPU utilization of the node.</p>

<p><img src="./notebooks/plots/BuildFarmRMWCPUConsumption.png" alt="Build Farm CPU Consumption"></p>

<h3 id="122-memory-utilization-in-a-spinning-node-by-rmw">1.2.2 Memory Utilization in a Spinning Node By RMW</h3>

<p>This plot shows the memory usage of a single, empty spinning node.
The node being empty means that it has no publishers, subscribers, services, actions, or timers attached.
Thus, this is a test of just the overhead of a node.
The 95% memory measurement indicates the 95% percentile (i.e. peak) memory utilization of the node.</p>

<p><img src="/TSC-RMW-Reports/humble/notebooks/plots/BuildFarmRMWMemoryConsumption.png" alt="Build Farm Memory Consumption"></p>

<h3 id="123-subscriber-cpu-utilization-latency-and-lost-messages-by-message-type-and-rmw">1.2.3 Subscriber CPU Utilization, Latency, and Lost Messages By Message Type and RMW</h3>

<p>In this plot, 1000 messages of the specified size were sent between a publisher and subscriber on the same machine.
For each message size, the plots show how many messages out of 1000 were received by the publisher, the average latency to receive each of the messages, and the average CPU utilization to receive the messages.
For this plot, Quality of Service options of best-effort, keep last, and a depth of 10 were used.</p>

<p><img src="/TSC-RMW-Reports/humble/notebooks/plots/PerfTestVsMsgSize.png" alt="Build Farm performance by message type"></p>

<h2 id="13-build-farm-test-discussion">1.3 Build Farm Test Discussion</h2>

<p>In the empty spinning node case, both RMW implementations are reasonably close in terms of CPU usage and memory consumption.
However, comparing the results to the <a href="/TSC-RMW-Reports/galactic/">2020 report</a>, both implementations now use more CPU and more memory than before.
It is unclear on whether this is due to changes in the middleware implementations, the RMW implementations, or in the ROS 2 core.</p>

<p>In terms of messages received both RMW implementations appear to perform well up until the 1MB message size.
After that point, we see a divergence in the implementations.
Cyclone DDS starts dropping messages at the 2MB size, and continues to drop more messages as the size increases.
Fast RTPS async drops a small number of messages at the 1MB and 2MB size, but starts dropping a large number of messages after that.
Fast RTPS sync mode receives all messages up until 4MB size, and starts dropping messages after that.
It should be noted that compared to the <a href="/TSC-RMW-Reports/galactic/">2020 report</a>, both implementations now deal with 2MB sizes better than before, with Fast RTPS showing a larger improvement.</p>

<p>For the message received latency, both RMW implementations are approximately the same up until the PointCloud512k message size.
Starting at the 1MB message size, the latency with Cyclone DDS approximately doubles for each step up in size.
Starting at the 1MB message size, the latency with Fast RTPS async goes up slowly until the 4MB size, where it spikes dramatically.
Fast RTPS sync has the best results here, with latency slowly increasing until the final test.
Compared to the <a href="/TSC-RMW-Reports/galactic/">2020 report</a>, Cyclone DDS sync and Fast RTPS async are approximately the same, with Fast RTPS sync showing a noticeable improvement.</p>

<p>Finally, for CPU usage all of the RMW implementations are about the same until the 60k message size.
After that, the Cyclone DDS CPU usage goes up quickly with the amount of data being sent, spiking at the 2MB size and then lowering from there.
The Fast RTPS async CPU usage spikes at 2MB, and then starts going down more dramatically.
In both of those cases, that is likely happening because more messages are being dropped after 2MB.
The Fast RTPS sync CPU usage goes up at the PointCloud512k size, drops dramatically for the 1MB, 2MB, and 4MB sizes, and then spikes again for the 8MB size.
This is an unexpected result, since CPU usage should increase as the data size goes up.
This may be a measurement error or other problem in that particular test.
Compared to the <a href="/TSC-RMW-Reports/galactic/">2020 report</a>, Cyclone DDS sync and Fast RTPS async are approximately the same, with Fast RTPS sync showing a very different performance curve.</p>

<h1 id="-2-rep-2004-code-quality-metrics"><a id="CodeQuality"></a> 2. REP-2004 Code Quality Metrics</h1>

<h2 id="21-overview-and-description">2.1 Overview and Description</h2>

<p>Code quality is an important metric for project health.
ROS 2 has defined various levels of package quality in <a href="https://ros.org/reps/rep-2004.html">REP-2004</a>.
Declaring a package to be in one of those quality levels means that it meets all of the requirements for that particular quality level.
The quality level of each of the middlewares and their RMW implementation is summarized below.
For more details, the reader is encouraged to look at the corresponding source repository for each middleware or RMW, where the quality level is declared in a file named QUALITY_DECLARATION.md or similar.</p>

<h2 id="22-results">2.2 Results</h2>

<table>
  <thead>
    <tr>
      <th>Package/Quality Metric</th>
      <th><a href="https://github.com/eclipse-cyclonedds/cyclonedds/blob/96a0374bdbb12a7d535dbc81092c3d87f2490ecb/CYCLONEDDS_QUALITY_DECLARATION.md">Cyclone DDS</a></th>
      <th><a href="https://github.com/ros2/rmw_cyclonedds/blob/2aa2cf527d079265195b2dca91bb9c82481be0c1/rmw_cyclonedds_cpp/QUALITY_DECLARATION.md">rmw_cyclonedds_cpp</a></th>
      <th><a href="https://github.com/eProsima/Fast-DDS/blob/4a27fbbbeb08ad83ffa10422eeaa201017382905/QUALITY.md">Fast RTPS</a></th>
      <th><a href="https://github.com/ros2/rmw_fastrtps/blob/daeeb8c7c57eec3df0a82aaf91a1b4e94aa889e3/rmw_fastrtps_cpp/QUALITY_DECLARATION.md">rmw_fastrtps_cpp</a></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Current Quality Level</td>
      <td>2</td>
      <td>4</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <td>1. Version Policy</td>
      <td>1. follows semver but major 0 is stable<br>2. current version is stable<br>3. <code class="language-plaintext highlighter-rouge">dds_</code> or <code class="language-plaintext highlighter-rouge">DDS_</code> symbols are public API, others may change<br>4. no major releases in stable allowed<br>5. no major releases in stable allowed<br>6. patch releases allowed, minor allowed after assessing ABI stability, major releases allowed if accompanied by <code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code> update</td>
      <td>1. follows semver<br>2. current version &lt; 1.0.0<br>3. public API is in the rmw headers<br>4. no major releases in stable allowed<br>5. no major releases in stable allowed<br>6. no major releases in stable allowed</td>
      <td>1. follows semver<br>2. current version is stable<br>3. API documentation <a href="https://fast-dds.docs.eprosima.com/en/latest/fastdds/api_reference/api_reference.html">available</a><br>4. no major releases in stable allowed<br>5. only minor releases break ABI<br>6. N/A</td>
      <td>1. follows semver<br>2. current version is stable<br>3. public API is in the headers<br>4. no major releases in stable allowed<br>5. no major releases in stable allowed<br>6. no major releases in stable allowed</td>
    </tr>
    <tr>
      <td>2. Change control</td>
      <td>1. changes must be in PR<br>2. DCO required<br>3. one review for merge (except when no reviewers available)<br>4. CI required to pass<br>5. documentation required</td>
      <td>1. changes must be in PR<br>2. DCO required<br>3. at least one review required for merge<br>4. CI required to pass<br>5. documentation required</td>
      <td>1. changes must be in a PR<br>2. DCO required<br>3. at least one review required for merge<br>4. CI required to pass<br>5. documentation required</td>
      <td>1. changes must be in PR<br>2. DCO required<br>3. at least one review required for merge<br>4. CI required to pass<br>5. documentation required</td>
    </tr>
    <tr>
      <td>3. Documentation</td>
      <td>1. concept documentation refers to DDS spec<br>2. API docs are embedded in the code<br>3. Eclipse Public License 2.0/Eclipse Distribution License 1.0<br>4. copyright statement included with the code</td>
      <td>1. features are documented via rmw API<br>2. public API docs in rmw, other API docs embedded in code<br>3. Apache 2.0 license<br>4. copyright statement included with the code</td>
      <td>1. features are documented<br>2. API reference is hosted at <a href="https://fast-dds.docs.eprosima.com/en/latest/fastdds/api_reference/api_reference.html">readthedocs</a><br>3. Apache 2.0 license<br>4. copyright statement included with the code</td>
      <td>1. some features are documented<br>2. API docs are embedded in the code<br>3. Apache 2.0 license<br>4. copyright statement included with the code</td>
    </tr>
    <tr>
      <td>4. Testing</td>
      <td>1. system tests cover features<br>2. tests cover all of the public API<br>3. line coverage should increase with changes<br>4. manual and nightly performance tests<br>5. uses coverity for static analysis</td>
      <td>1. system tests cover features<br>2. system tests cover APIs<br>3. line coverage should keep or increase, but decreases are allowed if justified<br>4. No performance tests<br>5. uses standard ROS linters and tests</td>
      <td>1. simulation tests cover features<br>2. tests cover typical usage of public API<br>3. line coverage should keep or increase, but decreases are allowed if justified<br>4. automatic performance test on changes<br>5. uses linters, but only for new code</td>
      <td>1. system tests cover features<br>2. unit and system tests cover the API<br>3. line coverage should increase with changes, but decreases allowed with justification<br>4. no performance tests<br>5. uses standard ROS linters and tests</td>
    </tr>
    <tr>
      <td>5. Dependencies</td>
      <td>1. no ROS deps<br>2. no ROS deps<br>3. OpenSSL* external dep</td>
      <td>1. all direct deps have Quality Declaration except for rosidl_typesupport_introspection_c{pp}<br>2. no optional direct runtime ROS deps<br>3. Eclipse Cyclone DDS claims to be at QL 2</td>
      <td>1. no ROS deps<br>2. no ROS deps<br>3. libasio, libtinyxml2, Fast CDR, foonathan_memory, and OpenSSL* external deps</td>
      <td>1. all direct runtime ROS deps declare quality level<br>2. no optional direct runtime ROS deps<br>3. Fast CDR/Fast RTPS claim to be at QL 1</td>
    </tr>
    <tr>
      <td>6. Platform</td>
      <td>1. supports all ROS 2 Tier 1 platforms</td>
      <td>1. supports all ROS 2 Tier 1 platforms</td>
      <td>1. supports all ROS 2 Tier 1 platforms</td>
      <td>1. supports all ROS 2 Tier 1 platforms</td>
    </tr>
    <tr>
      <td>7. Security</td>
      <td>1. conforms to <a href="https://ros.org/reps/rep-2006.html">REP-2006</a></td>
      <td>1. conforms to <a href="https://ros.org/reps/rep-2006.html">REP-2006</a></td>
      <td>1. <a href="https://github.com/eProsima/policies/blob/main/VULNERABILITY.md">Vulnerability disclosure policy</a></td>
      <td>1. Conforms to <a href="https://ros.org/reps/rep-2006.html">REP-2006</a></td>
    </tr>
  </tbody>
</table>

<p>* OpenSSL dependency for Cyclone DDS and Fast RTPS is optional, but used in ROS 2.</p>

<h2 id="23-discussion">2.3 Discussion</h2>

<p>Compared to last year, Cyclone DDS now has a Quality Level defined for <code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code>.</p>

<p>The packages implementing the DDS/RTPS protocol (<code class="language-plaintext highlighter-rouge">Cyclone DDS</code> and <code class="language-plaintext highlighter-rouge">Fast RTPS</code>) are comparable in most respects.
The key differences seem to be:</p>

<ul>
  <li>Cyclone DDS relies on the OMG DDS standard for documenting the features, while Fast RTPS has dedicated documentation</li>
  <li>Cyclone DDS has manual and nightly performance tests, while Fast RTPS has automated performance tests. Open Robotics build farm does nightly performance testing with both DDS implementations and rmw packages.</li>
  <li>Cyclone DDS conforms to REP-2006 for security vulnerability reporting, while Fast RTPS has its own, largely equivalent, security process</li>
</ul>

<p>The packages implementing the interface to ROS 2 (<code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code> and <code class="language-plaintext highlighter-rouge">rmw_fastrtps_cpp</code>) are generally comparable.
Here are some of the key differences:</p>

<ul>
  <li><code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code> has a major version number &lt; 1, while <code class="language-plaintext highlighter-rouge">rmw_fastrtps_cpp</code> has a major version number &gt; 1</li>
  <li><code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code> features are documented via the <code class="language-plaintext highlighter-rouge">rmw</code> API, while <code class="language-plaintext highlighter-rouge">rmw_fastrtps_cpp</code> relies on the README, the <code class="language-plaintext highlighter-rouge">rmw</code> docs, and the <code class="language-plaintext highlighter-rouge">Fast RTPS</code> docs</li>
  <li><code class="language-plaintext highlighter-rouge">rmw_cyclonedds_cpp</code> is missing a Quality Declaration for the <code class="language-plaintext highlighter-rouge">rosidl_typesupport_introspection_c{pp}</code> dependency, while <code class="language-plaintext highlighter-rouge">rmw_fastrtps_cpp</code> has a Quality Declaration for all dependencies
As a reminder, all of the quality levels for the various packages are self-declared.</li>
</ul>

<h1 id="-3-github-user-statistics"><a id="GitHubStats"></a> 3. GitHub User Statistics</h1>

<h2 id="31-overview-and-statistics">3.1 Overview and Statistics</h2>

<p>Responsiveness to issues and pull requests in a GitHub repository is a good proxy measurement for how quickly a given provider responds to their customers and
users.
The number of pull requests, and how quickly they are closed, can also give us an indication to how much development is taking place on a given code base and how quickly issues are being resolved.
To examine the responsiveness and development velocity of both RMW providers we used the GitHub API to collect commit, pull request, and issue data for the 180 days before the report was drafted on October 11, 2021.
The process of collecting this data was divided into two parts, data collection which can be found in <a href="https://github.com/osrf/TSC-RMW-Reports/blob/main/humble/notebooks/GetGitRMWDDSMetrics.ipynb">this notebook</a>, and data analysis which can be <a href="https://github.com/osrf/TSC-RMW-Reports/blob/main/humble/notebooks/PlotGithubStats.ipynb">found here</a>.</p>

<h2 id="32-github-engagement-results">3.2 GitHub Engagement Results</h2>

<h3 id="321-open-and-closed-pull-requests-in-the-previous-six-months">3.2.1 Open and Closed Pull Requests in the Previous Six Months</h3>

<p>The following plot gives the open and closed issues and pull requests broken down by both DDS implementation and RMW implementation.</p>

<p><img src="./notebooks/plots/PullRequestsAndIssues.png" alt="Open and closed pull requests and issues"></p>

<h3 id="322-cumulative-time-to-close-pull-requests-and-issues">3.2.2 Cumulative Time to Close Pull Requests and Issues</h3>

<p>These cumulative histograms give the percentage of issues and pull requests closed within a certain time frame over the 180 day sample period.</p>

<p><img src="/TSC-RMW-Reports/humble/notebooks/plots/IssueAndPRTurnAround.png" alt="Time to close pull requests and issues"></p>

<h2 id="33-github-metrics-discussion">3.3 GitHub Metrics Discussion</h2>

<p>Generally, for the six month period sampled, both providers are doing a great job responding to both issues and pull requests.
Both the main Cyclone DDS repository and the RMW implementation are slightly faster to close issues and pull requests than the Fast RTPS equivalents.
Fast RTPS has about 1.5 times as many pull requests and issues as Cyclone DDS.
This may be down to a number of factors, including the development practices, the number of ROS users, addressing bugs and feature requests, etc.</p>

<h1 id="-4-user-survey-results"><a id="Survey"></a> 4. User Survey Results</h1>

<h2 id="41-overview">4.1 Overview</h2>

<p>This section of the report is a user survey on ROS users’ feelings about their selected RMW implementation conducted between October 6th and 13th 2021.
The survey was <a href="https://discourse.ros.org/t/survey-default-dds-implementation-for-ros-2-humble-due-10-12-2021/22575">posted to ROS Discourse</a> and provided ROS 2 users with a chance to rate the performance of their RMW as well as give a narrative description of their experience.
In total there were 88 responses with 47 users reporting that they use Cyclone DDS  and 41 users reporting they use Fast RTPS.
Nearly all of the respondents were ROS 2 users with approximately 85% of them presently working with ROS 2 Foxy or Galactic.</p>

<p>In the following section we summarize the data and where possible provide the descriptive statistics for both RMWs as well for the ROS community.
Section 4.2 gives a summary of the results and section 4.3 includes excerpts of narratives submitted by ROS 2 users.</p>

<h2 id="42-overall-survey-results">4.2 Overall Survey Results</h2>

<p>For our 2021 ROS 2 User Survey we asked participants to self report the both the version of ROS they used and their preferred DDS implementation.
These data are summarized in plot 4.2.1.</p>

<h3 id="421-ros-distro-and-preferred-dds-vendor">4.2.1 ROS Distro and Preferred DDS Vendor</h3>
<p><img src="/TSC-RMW-Reports/humble/notebooks/plots/ROS2Version.png" alt="ROS 2 Distro used by the Respondents broken down by preferred DDS implementation"></p>

<p>More than half of all respondents are currently using ROS 2 Foxy Fitzroy, the current LTS ROS 2 Release, with another 40% using either ROS 2 Galactic or ROS 2 Rolling Ridley.
A small minority continue to use ROS 2 Dashing, or Eloquent or do not use ROS 2.
These results were fairly consistent across DDS vendors.</p>

<p>This year’s survey was extremely direct and asked respondents which DDS vendor they would recommend to the ROS 2 TSC as the Humble default.
Each respondent was asked to select their preferred vendor and also to submit their confidence in that selection on scale from one to ten (1 – low confidence, 10 – high confidence).
These results are summarized in figure 4.2.2.</p>

<h3 id="422-vendor-recommendation-and-confidence-score">4.2.2 Vendor Recommendation and Confidence Score</h3>
<p><img src="/TSC-RMW-Reports/humble/notebooks/plots/ROS2Choice.png" alt="Preferred DDS Implementation and Confidence in that Decision"></p>

<p>Based on the user feedback there was a slight preference for Cyclone DDS (47 responses vs. 41 responses) with the Cyclone users also being slightly more confident in their choice.</p>

<p>In our survey we asked each community member if they had tried both DDS vendors before making their recommendation to the TSC.
These data are captured in figure 4.2.3.</p>

<h3 id="423-percentage-of-users-who-tried-both-tier-one-dds-vendors">4.2.3 Percentage of Users Who Tried both Tier One DDS Vendors</h3>
<p><img src="/TSC-RMW-Reports/humble/notebooks/plots/SwitchChoice.png" alt="Percentage of Respondents who Tried both DDS Implementations and the Outcome"></p>

<p>Slightly less than two thirds of those responding to the survey had tried both Tier 1 DDS vendors.
Of those who tried both vendors the majority of them decided to use Cyclone DDS as their default DDS implementation.</p>

<p>Our survey also tried to gauge the net promoter score of each Tier 1 DDS implementation.
A <a href="https://en.wikipedia.org/wiki/Net_promoter_score">net promoter score</a> is a market research metric that asks a user, “On a scale of one to ten, how likely are you to recommend this product to a friend.”
A histogram of net promoter scores for each Tier 1 DDS Vendor is provided in figure 4.2.4.</p>

<h3 id="424-histogram-of-net-promoter-scores">4.2.4 Histogram of Net Promoter Scores</h3>
<p><img src="/TSC-RMW-Reports/humble/notebooks/plots/DDSNPS.png" alt="Net Promoter Score Histogram"></p>

<p>The histograms of both Tier 1 DDS Vendors are fairly similar, with the majority of users scoring their DDS implementation highly.
Both vendors have a median score of 9, but Fast RTPS has a slightly higher mean score of 8.93 compared to Cyclone DDS’s score 8.53.</p>

<h2 id="section-43-narrative-responses-from-ros-2-users">Section 4.3 Narrative Responses from ROS 2 Users</h2>

<h3 id="431-how-do-users-evaluate-dds-vendors">4.3.1 How Do Users Evaluate DDS Vendors</h3>

<p>In our survey we asked participants to discuss how they evaluated the Tier 1 DDS vendors, below are some of their responses.</p>

<p>Some users were concerned with the communities behind the development (this sentiment was echoed in a number of responses.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>At this stage, CycloneDDS and FastDDS are similar enough from a technical and
performance standpoint that my evaluation has shifted more towards a qualitative
evaluation of the organizations/developers behind the implementation,
particularly with respect to how eager and responsive the developers are to
accommodating the needs and requests of the community. I should note that we
still internally use RTI Connext as our "mission critical/battle hardened" DDS
vendor of choice for the most important components of our stack (these being
pure DDS and not ROS2-based), having almost eight years of experience and
success with their product.
</code></pre></div></div>

<p>Other survey participants used their CI systems to evaluate performance. Here is one such example:</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>[We] simply [monitor] the pass/fail rates and test flakyness of [our] CI over
the matrix of RMW vendors. Feel free to review the historic trend on our
[nightly CI. At] this stage, CycloneDDS and FastDDS are similar enough from a
technical and performance [standpoint].
</code></pre></div></div>

<p>Many users simply tried both vendors, like this user.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>[We] monitored performance of dds implementations and made several PR
contributions to both of them. Compared DDS implementations in different use
cases (multi process shared memory, multiple network interfaces, etc)
</code></pre></div></div>

<h3 id="432-cyclone-dds-users">4.3.2 Cyclone DDS Users</h3>

<p>Our survey asked Cyclone users what they thought about Cyclone DDS and why they think it should be the default.
One user claimed the out of the box experience wasn’t great.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>I have 100% confidence in Cyclone as a middleware. I have encountered a few
instances of customers complaining about inconsistent message delivery from
their laptops. Every single time this has been the case, those customers have
been running fast instead of Cyclone (since it is the default), and it is always
fixed immediately when changing to Cyclone.
</code></pre></div></div>

<p>Other users claimed that they have had success in production with Cyclone, like this user.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>We have been using this DDS implementation at scale (100 AMR over unreliable
wifi) for over a year with next to no issue. In comparison, we have used
FastRTPS in the past with a lot of issues.
</code></pre></div></div>

<p>Multiple users preferred using Cyclone because of its feature set and its open-source model.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>I like that it is open-source (like ROS) and that the developers are accessible,
responsive, and very interested to learn about and accommodate your
application. I also think the integration of Iceoryx will be game-changing for
how we write ROS code.
</code></pre></div></div>

<h3 id="433-fast-rtps-users">4.3.3 Fast RTPS Users</h3>

<p>Our survey also asked Fast RTPS users what they liked about Fast RTPS and why they thought it should be the default.
Many users claimed that the code quality was much better, like the user below.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>Fastdds is a production level DDS implementation. Performance is good, but what
strikes the most is the quality of its code. It's maintained through a serious
review process, it's easy to look and add features. The code does not contain
hacks or subtleties. There are a lot of documentation and examples.
</code></pre></div></div>

<p>Other users claimed that the Fast RTPS development road map made software development easier:</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>One of our requirements is to ensure data persistency and right now only Fast
DDS have this feature implemented. Cyclone DDS was not an option for the
moment. Their roadmap published last year said that it would be available soon
and I would have liked to test it and do some benchmarking, but I don't think it
has been released yet.
</code></pre></div></div>

<p>Finally, some Fast RTPS users just thought the performance was just better.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>It [Fast RTPS] turns out to be both more stable and faster in our benchmarks.
</code></pre></div></div>

<h3 id="434-what-caused-users-to-switch-to-cyclone-dds">4.3.4 What Caused Users to Switch to Cyclone DDS</h3>

<p>For ROS users who switched to Cyclone DDS from Fast RTPS we asked them what motivated that change.
The survey asked, “Before you go, is there anything you would like to tell the ROS 2 TSC about your experience with <strong>Fast RTPS</strong>? Did you switch DDS vendors? If so, why?”</p>

<p>For some users the switch was motivated by unpatched bugs.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>We switched from fastdds to cyclonedds as after an official foxy release in the
beginning of the year, there was a serious bug in released fastdds version
related to a memory transport in a discovery daemon (if I remember correctly)
</code></pre></div></div>

<p>Several users reported issues with crashing services that were fixed by switching to Cyclone.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>Crashing services; RMW or DDS layer exceptions being thrown; generally
unreliable and requiring significant DDS configuration file customization to
get reasonable behavior for mobile robot systems. Several tickets filed in Nav2
which were trivially solved for users by switching the Cyclone
</code></pre></div></div>

<p>Other users thought the performance differences were negligible but the developer experience with Cyclone was much better.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>Experience with the actual products has been about the same. Experience with
the personnel at FastDDS has been awful.
</code></pre></div></div>

<p>Other users had difficulties  with installation and concerns about the complexity of using FastDDS.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>I experienced less problems during the installation and troubleshooting with
Cyclone DDS than Fast RTPS. Moreover, Cyclone DDS is more lightweight in our
target platforms.
</code></pre></div></div>

<h3 id="434-what-caused-users-to-switch-to-fast-rtps">4.3.4 What Caused Users to Switch to Fast RTPS</h3>

<p>For ROS users who switched from Cyclone DDS from Fast RTPS we asked them what motivated that change.
The survey asked, “Before you go, is there anything you would like to tell the ROS 2 TSC about your experience with <strong>Cyclone DDS</strong>  Did you switch DDS vendors? If so, why?”</p>

<p>For some users the switch was motivated by performance issues.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>In most cases Cyclone DDS was working well, but we had some strange behaviors,
stability issues (apparently losing some packets) and found out its performance
not as good as FastDDS.
</code></pre></div></div>

<p>Other users thought the performance between the two vendors were similar but had concerns about code quality.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>I tested and evaluated Cyclone DDS in detail. Despite its performance being
better than Fastdds in some metrics, I wouldn't base a product on it. The code
is quite messy and basically maintained and developed by a single person. It
still lacks many features wrt fastdds and it looks like support for new features
always results in increasing exponentially the complexity of the
code. Cyclonedds is definitely very promising, but it shouldnt be a default
implementation until it goes through a deep cleanup and refactor to be easier to
debug and more scalable. The amount of documentation is also very small and this
makes it extremely hard to try and use some of its features.
</code></pre></div></div>

<p>For other users the choice was based on the availability of certain features.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>I am interested in contributing ROS2 APIs that enable productive connectivity to
5G networks. I switched to Fast RTPS because they were the only ones who
implemented support for 5G network connectivity API called "unique network
flows" that are part of Galactic.
</code></pre></div></div>

<p>Some users thought that the documentation and support for Fast RTPS was much better.</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>We tried to switch to cyclone when we run into some issues with our
containerization, however, there were other problems with Cyclone as well.
Furthermore, we got more quick support from FastDDS, which also pointed us out
to their documentation which was quite extensive.
</code></pre></div></div>

<h1 id="-5-dds-provider-responses"><a id="DDSProviderResponses"></a> 5. DDS provider responses</h1>

<h2 id="51-overview">5.1 Overview</h2>

<p>As previously mentioned, each of the candidate DDS providers was given a <a href="/TSC-RMW-Reports/humble/dds_provider_question_template.html">questionnaire</a> to respond to.
The questions provided all came from TSC members, and represent a subset of the concerns facing the ROS 2 community.
The responses from each of the providers is below:</p>

<ul>
  <li>
    <p><a href="/TSC-RMW-Reports/humble/eclipse-cyclonedds-report.html">2021 Eclipse Cyclone DDS ROS Middleware Evaluation Report with iceoryx and Zenoh</a></p>
  </li>
  <li>
    <p><a href="/TSC-RMW-Reports/humble/eProsima-response.html">Fast RTPS TSC RMW report 2021</a></p>
  </li>
</ul>

<h2 id="52-discussion">5.2 Discussion</h2>

<p>The two reports were taken with different hardware by different people at different times.
<em>Additionally, the Fast RTPS response is using <a href="https://github.com/osrf/TSC-RMW-Reports/blob/main/humble/ros2.repos">this ros2.repos</a> file from August 31, 2021 which was the one specified in the questionnaire.
Cyclone DDS had issues using the specified repos file, so they used Galactic Patch Release 1 instead.</em>
All of these factors mean that the two reports are not directly comparable in any meaningful sense.
The reader is encouraged to look at the way in which the providers answered the concerns coming from the community.
This can give insight into how, and how much, a provider is thinking about any particular issue.</p>

<p>Since the two reports are vastly different, a detailed comparison will not be provided here.
Here are some interesting points the editors noticed while reading the reports:</p>

<ul>
  <li>
    <p>Looking at the provider responses, Cyclone DDS answered all of the questions.  Fast RTPS answered all of the questions except for the one that says “How well does the implementation work out-of-the-box over WiFi?”.</p>
  </li>
  <li>
    <p>For the performance scaling tests, the Cyclone DDS plots show up to 50 subscribers, while the Fast DDS ones only show up to 10 subscribers.</p>
  </li>
  <li>
    <p>In terms of memory usage, both of the reports agree that Fast RTPS has higher memory usage in the usual cases.  According to the eProsima report, this is because Fast RTPS support more configurations and options.</p>
  </li>
  <li>
    <p>Service scalability suffers on both because all replies are sent to all clients, which would be improved by using Content Filtering.  Both middleware implementations have Content Filtering support, but as of this writing neither RMW implementation supports it.</p>
  </li>
  <li>
    <p>For the WiFi answers, both providers mentioned that additional configuration is needed in order to make WiFi work better.  In the Fast RTPS case, this is by either providing a list of Initial Peer node (through XML configuration), or by setting up a Discovery Server.  In the Cyclone DDS case, this is by deploying Zenoh to deal with WiFi communications in a different way.</p>
  </li>
</ul>


      <footer class="site-footer">
        
          <span class="site-footer-owner"><a href="https://github.com/osrf/TSC-RMW-Reports">TSC-RMW-Reports</a> is maintained by <a href="https://github.com/osrf">osrf</a>.</span>
        
        <span class="site-footer-credits">This page was generated by <a href="https://pages.github.com">GitHub Pages</a>.</span>
      </footer>
    </main>
  

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML&amp;delayStartupUntil=configured"></script><script id="texAllTheThingsPageScript" type="text/javascript" src="chrome-extension://cbimabofgmfdkicghcadidpemeenbffn/js/pageScript.js" inlinemath="[[&quot;$&quot;,&quot;$&quot;],[&quot;[;&quot;,&quot;;]&quot;]]" displaymath="[[&quot;$$&quot;,&quot;$$&quot;],[&quot;\\[&quot;,&quot;\\]&quot;]]" skiptags="[&quot;script&quot;,&quot;noscript&quot;,&quot;style&quot;,&quot;textarea&quot;,&quot;pre&quot;,&quot;code&quot;]" ignoreclass="false" processclass="false"></script><remove-web-limits-iqxin id="rwl-iqxin" class="rwl-exempt" style="position: fixed; top: 0px; left: 0px;"><qxinbutton type="qxinbutton" id="rwl-setbtn"> set </qxinbutton> <lalala style="cursor:move; font-size:12px;">限制解除</lalala> <input type="checkbox" name="" id="black_node"><style type="text/css">#rwl-iqxin{position:fixed;transform:translate(-95px,0);width:85px;height:25px;font-size:12px;font-weight: 500;font-family:Verdana, Arial, '宋体';color:#fff;background:#333;z-index:2147483647;margin: 0;opacity:0.05;transition:0.3s;overflow:hidden;user-select:none;text-align:center;white-space:nowrap;line-height:25px;padding:0 16px;border:1px solid #ccc;border-width:1px 1px 1px 0;border-bottom-right-radius:5px;box-sizing: content-box;}#rwl-iqxin input{margin: 0;padding: 0;vertical-align:middle;-webkit-appearance:checkbox;-moz-appearance:checkbox;position: static;clip: auto;opacity: 1;cursor: pointer;}#rwl-iqxin.rwl-active-iqxin{left: 0px;transform:translate(0,0);opacity: 0.9;height: 32px;line-height: 32px}#rwl-iqxin label{margin:0;padding:0;font-weight:500;}#rwl-iqxin #rwl-setbtn{margin: 0 4px 0 0;padding: 0 0 0 4px;border: none;border-radius: 2px;cursor: pointer;background: #fff;color: #000;} </style></remove-web-limits-iqxin><iframe src="about:blank" style="display: none;"></iframe></body></html>
