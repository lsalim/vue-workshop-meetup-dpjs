<template>
  <div id="app">   
<body class="light" id="body">
<Header />
<Meetups />
<Footer />
</body>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Meetups from './components/Meetups.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,
    Meetups,
    Header,
    Footer
  }
}
</script>

<style>
/* http://meyerweb.com/eric/tools/css/reset/
   v2.0 | 20110126
   License: none (public domain)
*/
@import url("https://fonts.googleapis.com/css?family=Montserrat:400,500,600,700");
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}

/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
  display: block;
}

body {
  line-height: 1;
}

ol, ul {
  list-style: none;
}

blockquote, q {
  quotes: none;
}

blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

/***-------------------- HEADER STYLE --------------------------***/
header {
  background: #5A3CC8 url("assets/img/illustrations/illustrations.png") top center no-repeat;
  height: 250px;
  border-bottom-left-radius: 100px;
  border-bottom-right-radius: 100px;
}

header ul {
  max-width: 1000px;
  margin: 0 auto;
  padding-top: 40px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

header ul h3 {
  font-family: 'Montserrat', sans-serif;
  color: white;
  font-size: 28px;
  text-align: center;
  font-weight: 400;
}

header p {
  text-align: center;
  margin-top: 40px;
}

header p input {
  width: 400px;
  height: 30px;
  border-radius: 6px;
  border: 2px solid #321D7C;
  text-align: center;
  outline: none;
  font-family: 'Montserrat', sans-serif;
}

#theme-switcher {
  display: inline-block;
  width: 20px;
  height: 20px;
  outline: none;
}

.light #theme-switcher {
  background: url(assets/img/icons/icon_sun.svg) center center no-repeat;
}

.dark #theme-switcher {
  background: url(assets/img/icons/icon_moon.svg) center center no-repeat;
}

/***-------------------- GLOBAL STYLE --------------------------***/
body.light {
  background: white;
}

body.dark {
  background: #292A2E;
}

body {
  transition: all 0.4s ease-in-out;
}

/***-------------------- FOOTER STYLE --------------------------***/
footer {
  background: #5A3CC8;
  bottom: 0px;
  width: 100%;
  height: 60px;
}

footer p {
  text-align: center;
  color: white;
  font-family: "Montserrat", sans-serif;
  line-height: 60px;
}

/***-------------------- EVENT CARD STYLE --------------------------***/
.event {
  max-width: 600px;
  height: 230px;
  box-shadow: 0 5px 30px 2px rgba(0, 0, 0, 0.1);
  display: flex;
  padding: 30px;
  box-sizing: border-box;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  transition: all 0.4s ease-in-out;
}

.event .metadata {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  padding-top: 30px;
}

.event .metadata li {
  margin-bottom: 26px;
  display: flex;
  align-items: center;
}

.event .metadata li span:last-child {
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  padding-left: 10px;
  font-size: 15px;
}

.event .metadata h1 {
  font-family: "Montserrat", sans-serif;
  font-size: 28px;
  font-weight: 600;
}

.event .metadata .icon-date {
  display: inline-block;
  width: 20px;
  height: 20px;
}

.event .metadata .icon-location {
  display: inline-block;
  width: 20px;
  height: 27px;
}

.meetup-avatar img {
  border-radius: 60px;
  box-shadow: 0 0 30px 5px rgba(0, 0, 0, 0.15);
}

.light .event {
  background: white;
}

.light .event .icon-date {
  background: url(assets/img/icons/icon_calendar_light.svg) left center;
}

.light .event .icon-location {
  background: url(assets/img/icons/icon_place_light.svg);
}

.light .event .metadata h1 {
  color: #333333;
}

.light .event .metadata li span:last-child {
  color: rgba(0, 0, 0, 0.5);
}

.dark .event {
  background: #313238;
}

.dark .event .icon-date {
  background: url(assets/img/icons/icon_calendar_dark.svg) left center;
}

.dark .event .icon-location {
  background: url(assets/img/icons/icon_place_dark.svg);
}

.dark .event .metadata h1 {
  color: #EEECEC;
}

.dark .event .metadata li span:last-child {
  color: rgba(238, 236, 236, 0.7);
}

#meetups.details li:first-child .event {
  border-bottom-right-radius: 0;
}

/***-------------------- DETAILS PAGE STYLE --------------------------***/
#meetups {
  margin-top: -80px;
  margin-bottom: 100px;
}

#meetups li {
  margin-bottom: 24px;
}

#meetups li:first-child .event {
  border-top-left-radius: 40px;
}

#meetups li:last-child .event {
  border-bottom-right-radius: 40px;
}

#meetup-details {
  box-sizing: border-box;
  max-width: 600px;
  margin: 20px auto;
  box-shadow: 0 5px 30px 2px rgba(0, 0, 0, 0.1);
  padding: 40px 34px;
  border-bottom-right-radius: 40px;
}

#meetup-details p {
  font-family: "Montserrat", sans-serif;
}

#meetup-details ul .speaker-infos {
  display: flex;
  align-items: center;
}

#meetup-details ul .speaker-infos p:first-child {
  margin-right: 10px;
}

#meetup-details ul .speaker-infos .meta p:first-child {
  margin-bottom: 10px;
  font-size: 18px;
  font-weight: 600;
}

#meetup-details ul .speaker-infos .meta p:last-child {
  margin-top: 10px;
  font-size: 14px;
  font-weight: 500;
}

#meetup-details ul .talk-title {
  margin-top: 20px;
  font-size: 18px;
  font-weight: 600;
  color: #5A3CC8;
  padding-bottom: 40px;
}

#meetup-details ul .talk-title i.icon-talk {
  display: inline-block;
  width: 20px;
  height: 20px;
  margin-right: 2px;
  background: url(assets/img/icons/icon_speak.svg);
}

#meetup-details ul li:last-child {
  margin-bottom: 0;
}

#meetup-details ul li:last-child p.talk-title {
  padding: 0;
  border-bottom: none;
}

.light #meetup-details {
  background: white;
}

.light #meetup-details .meta p:first-child {
  color: #333333;
}

.light #meetup-details .meta p:last-child {
  color: rgba(51, 51, 51, 0.6);
}

.light #meetup-details .talk-title {
  border-bottom: 1px solid #E3E3F8;
}

.dark #meetup-details {
  background: #313238;
}

.dark #meetup-details .meta p:first-child {
  color: #EEECEC;
}

.dark #meetup-details .meta p:last-child {
  color: rgba(238, 236, 236, 0.7);
}

.dark #meetup-details .talk-title {
  border-bottom: 1px solid rgba(255, 255, 255, 0.3);
}

</style>
