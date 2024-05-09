<script setup>
  import { ref } from 'vue';
  
  const articleHTML = ref();

  fetch('1data.json')
    .then(response => response.json())
    .then(data => {
      articleHTML.value = data.article;
    })

</script>

<template>
  <h1>"Free Palestine": US Airman Dies After Setting Himself On Fire Over Gaza</h1>
  
  <main>
  
  <article><p><span class="bold">Washington:</span> A US airman has died after setting himself on fire outside the Israeli embassy in Washington at the weekend in protest over the war in Gaza, the Air Force said Monday.
  The shocking act was an escalation of recent protests across the United States against Israel's actions in Gaza, where with US support it is waging a retaliatory war for an attack on October 7 by Hamas militants.</p>
  
  <p>Emergency responders on Sunday had rushed to the scene in response to a "call for person on fire outside the Israeli Embassy," the capital city's fire department.</p>
  
  <p>The unnamed man had filmed himself shouting "Free Palestine" as he lit himself on fire, according to footage shared on social media.</p>
  
  <p>He was transported to hospital with "critical life-threatening injuries," the fire department said, and an Air Force spokeswoman said Monday morning he had died Sunday night.</p>
  
  <p>A spokesperson for the Israeli embassy said no staff were injured.</p>
  
  <p>In the video, the man wearing military fatigues and declaring he will "not be complicit in genocide" before dousing himself in liquid, lighting himself on fire and yelling "Free Palestine!" until he collapses.</p>
  
  <p>The video was reportedly first shared in a livestream on the social platform Twitch.</p>
  
  <p><span class="bold">- Domestic and international pressure -</span></p>
  
  <p>With the death toll in Gaza nearing 30,000, according to the Hamas-run health ministry there, international pressure has been increasing on the United States to rein in ally Israel and call for a ceasefire.</p>
  
  <p>The war broke out after Hamas launched an unprecedented October 7 attack which killed 1,160 people in Israel, mostly civilians, according to an AFP tally of official figures.</p>
  
  <p>Militants also took about 250 hostages, 130 of whom remain in Gaza, including 31 presumed dead, according to Israel.</p>
  
  <p>Washington last week blocked a UN Security Council resolution calling for an immediate ceasefire in Gaza, its third such use of its veto on the matter.</p>
  
  <p>Some voters in Joe Biden's Democratic Party are attempting to press the president on the issue, with groups of Arab American voters in Michigan pledging to vote "uncommitted" or write in "Free Palestine" on their ballots in the state's primary Tuesday.</p>
  
  <p>The White House has tried to assuage Arab and Muslim voters' concerns in part by portraying the president as frustrated with Benjamin Netanyahu's government.</p>
  
  <p>But US weapons have flowed to Israel since October 7, while Washington's efforts to broker a second pause in fighting have so far failed.</p>
  
  <p>In an update on ongoing multinational talks Sunday, the United States said an "understanding" had emerged on a possible deal for Hamas to release hostages and for a new ceasefire in the Gaza war.</p>
  
  <p>Domestic demonstrations have typically involved peaceful street protests, though in December a person outside the Israeli consulate in Atlanta also set themself on fire.</p></article>
  
  <a href="https://www.ndtv.com/world-news/free-palestine-us-airman-set-himself-on-fire-outside-israeli-embassy-5131489" target="_blank">original news page</a>

  <div class="summary">
    <p class="center">总结</p>
    <p>1.文本居中 text-align: center;</p>
    <p>2.行间距 line-height: xx;</p>
    <p>3.缩进 text-indent: xx;</p>
  </div>

  </main>
</template>

<style scoped>
  * {

  }

  h1 {
    text-align: center;
    font-family: serif;
  }

  main {
    --left-and-right-margin-value: 5em;

    margin-left: var(--left-and-right-margin-value);
    margin-right: var(--left-and-right-margin-value);
  }

  span {
    font-family: serif;
  }

  .bold {
    font-weight: bold;
  }

  p {
    font-family: sans-serif;
    /* 控制行间距 */
    line-height: 1.6em;
  }

  article > p {
    /* 控制缩进 */
    text-indent: 2em;
  }

  a {
    text-decoration: underline;
  }

  a:hover {
    text-decoration: none;
  }

  .center {
    text-align: center;
  }

  .summary {
    color: white;
    background-color: rgba(18, 17, 22, 0.733);
    border-radius: 2em;
    padding-top: 1em; padding-bottom: 1em;  padding-left: 2em; padding-right: 2em;
    border: 1px solid;
    margin: 1em;
    width: fit-content;
  }

</style>