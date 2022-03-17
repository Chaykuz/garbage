

```css

/* AUTO=body_background */ body { background: url(/assets/background/noisy_net.png) repeat; }
@import url(https://raw.githubusercontent.com/kaurkaur/Shikimori/master/CSS/HistoryDates.css);
@import url(https://gist.githubusercontent.com/grin3671/d994b47c010aabfd06cba7b9b1edcf03/raw/mobileHistory.css);

/* AUTO=page_border */ .l-page:before, .l-page:after, .l-footer:before, .l-footer:after { display: none; }
.l-top_menu-v2 {
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
}
.l-page {
  margin-top: 46px;
}
.b-comments-notifier {
  top: 46px !important;
}
.l-top_menu-v2 {
  max-width: 1200px;
  margin: auto;
}

.x1000 .l-top_menu-v2 {
  max-width: 1000px;
}

.b-comments-notifier {
  top: 0px !important;
}
.l-top_menu-v2 .submenu > a:hover,
.l-top_menu-v2 .menu-dropdown > button:not(.mobile):hover,
.l-top_menu-v2 .menu-dropdown > button:not(.mobile) a:hover {
  box-shadow: 0 0 20px rgba(128, 0, 255,.6),
              0 0 20px rgba(128, 0, 255,1) inset;
  transition: 0.3s;
}

.b-feedback {
display: none;
}
  
.activity .graph.vertical .line .bar {
  box-sizing: content-box;
  transform: translateY(1px);
  transform-origin: center bottom;
  animation-fill-mode: both;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  animation-duration: 1.5s;
  animation-name: activity;
}
.activity .graph.vertical .line .bar:hover {
  animation-name: none;
  transform: none;
}
.activity .graph.vertical .line:nth-of-type(6n+2) .bar {
  animation-delay: -.25s;
}
.activity .graph.vertical .line:nth-of-type(6n+4) .bar {
  animation-delay: -.5s;
}
.activity .graph.vertical .line:nth-of-type(6n+3) .bar {
  animation-delay: -.75s;
}
.activity .graph.vertical .line:nth-of-type(6n+6) .bar {
  animation-delay: -1s;
}
.activity .graph.vertical .line:nth-of-type(6n+5) .bar {
  animation-delay: -1.25s;
}
@keyframes activity {
  0%, 100% {
    transform: translateY(1px);
  }
  50% {
    transform: translateY(7px);
  }
}
  }

/*
 * Circle Anime Manga Bar
 * Shikimori.org – CSS Theme
 * MIT License
 * Copyright (c) 2017 kaur
 */

/*COLORS*/
/*Аниме Просмотрено*/
.c-lists-info .b-stats_bar.anime .bar > div.first:before,
.c-lists-info .b-stats_bar.anime .bar > div.first:after,
.c-lists-info .b-stats_bar.anime .stat_names .stat_name a[href*="completed"]:before{
	border-color:transparent;
	background-color:#4682B4
}
/*Аниме Запланировано*/
.c-lists-info .b-stats_bar.anime .bar > div.second:before,
.c-lists-info .b-stats_bar.anime .bar > div.second:after,
.c-lists-info .b-stats_bar.anime .stat_names .stat_name a[href*="planned"]:before,
.c-lists-info .b-stats_bar.anime .stat_names .stat_name a[href*="watching"]:before,
.c-lists-info .b-stats_bar.anime .stat_names .stat_name a[href*="on_hold"]:before{
	border-color:transparent;
	background-color:#79A9CF
}

/*Манга Прочитано*/
.c-lists-info .b-stats_bar.manga .bar > div.first:before,
.c-lists-info .b-stats_bar.manga .bar > div.first:after,
.c-lists-info .b-stats_bar.manga .stat_names .stat_name a[href*="completed"]:before{
	border-color: transparent;
	background-color:#B78BC7
}
/*Манга Запланировано*/
.c-lists-info .b-stats_bar.manga .bar > div.second:before,
.c-lists-info .b-stats_bar.manga .bar > div.second:after,
.c-lists-info .b-stats_bar.manga .stat_names .stat_name a[href*="planned"]:before,
.c-lists-info .b-stats_bar.manga .stat_names .stat_name a[href*="watching"]:before,
.c-lists-info .b-stats_bar.manga .stat_names .stat_name a[href*="on_hold"]:before{
	border-color: transparent;
	background-color:#EDACD9
}
/*Оба Графика Брошено*/
.c-lists-info .b-stats_bar .bar,
.c-lists-info .b-stats_bar .stat_names .stat_name a[href*="dropped"]:before{
	border-color: transparent;
	background-color: #AAAAAA
}
/*Дырка в графике указать, transparent для прозрачной дырки*/
.c-lists-info .b-stats_bar .bar:before{
	background: #fff; 
}

/*COLORS:END*/
.c-lists-info .b-stats_bar{
	width: 49%;
	display: inline-block;
	padding:5px;
	position: relative;
}
.c-lists-info .b-stats_bar:first-child{border-right:1px dotted #ddd}
.c-lists-info .b-stats_bar .stat_names .stat_name:after{display: none}

/*Блок списка*/
.c-lists-info .b-stats_bar .stat_names{
	display: flex;
	position: absolute;
	top:33px;
	left:165px;
	height:150px;
	flex-direction: column;
	justify-content: center;
}

/*Ссылка*/
.c-lists-info .b-stats_bar .stat_names .stat_name a{
	display: inline-block;
	font-size: 12px;
	position: relative;
	line-height: 25px;
}

/*На х1000 обрезает число и загоняет текст под многоточее*/
.x1000 .c-lists-info .b-stats_bar .stat_names a{
	font-size: 11px;
	width: 90px;
	overflow: hidden;
	white-space: nowrap;
	text-overflow: ellipsis;
}
.x1000 .c-lists-info .b-stats_bar .stat_names a span{
	display: none;
}
/*Круг цветового индикатора*/
.c-lists-info .b-stats_bar .stat_names .stat_name a:before {
	content: "";
	display: inline-block;
	width: 12px;
	height:12px;
	background: #fff;
	margin-right: 5px;
	vertical-align: middle;
	border:1px solid #ddd;
	border-radius: 50%;
}

/*CIRCLE BAR*/
.c-lists-info .b-stats_bar .bar,
.c-lists-info .b-stats_bar .bar > div{
	height:150px!important;
	width:150px!important;
}
.c-lists-info .b-stats_bar .bar{
	position: relative;
	text-align: center;
	border-radius: 50%;
	margin: 10px 0;
}
.c-lists-info .b-stats_bar .bar:before{
	content:"";
	width:50px;
	height:50px;
	border-radius: 50%;
	position: absolute;
	z-index: 100;
	left:50px;
	top:50px;
}
.c-lists-info .b-stats_bar .bar > div{
	clip: rect(0px, 150px, 150px, 75px);
	background-color: transparent!important;
	font-size: 0!important;
	position: absolute;
	left: 0;
	top:0;
}
.c-lists-info .b-stats_bar .bar > div:before,
.c-lists-info .b-stats_bar .bar > div:after{
	content: "";
	position: absolute;
	right: 0;
	border: 75px solid #333;
	clip: rect(0px, 75px, 150px, 0px);
	border-radius: 50%;
	transform: rotate(0deg);
}
.c-lists-info .b-stats_bar .bar > div.third{display: none}
.c-lists-info .b-stats_bar .bar > div.second{transform: scale(-1, 1)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 1."]:before{transform: rotate(3.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 2."]:before{transform: rotate(7.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 3."]:before{transform: rotate(10.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 4."]:before{transform: rotate(14.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 5."]:before{transform: rotate(18deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 6."]:before{transform: rotate(21.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 7."]:before{transform: rotate(25.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 8."]:before{transform: rotate(28.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 9."]:before{transform: rotate(32.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 10."]:before{transform: rotate(36deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 11."]:before{transform: rotate(39.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 12."]:before{transform: rotate(43.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 13."]:before{transform: rotate(46.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 14."]:before{transform: rotate(50.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 15."]:before{transform: rotate(54deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 16."]:before{transform: rotate(57.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 17."]:before{transform: rotate(61.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 18."]:before{transform: rotate(64.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 19."]:before{transform: rotate(68.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 20."]:before{transform: rotate(72deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 21."]:before{transform: rotate(75.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 22."]:before{transform: rotate(79.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 23."]:before{transform: rotate(82.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 24."]:before{transform: rotate(86.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 25."]:before{transform: rotate(90deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 26."]:before{transform: rotate(93.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 27."]:before{transform: rotate(97.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 28."]:before{transform: rotate(100.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 29."]:before{transform: rotate(104.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 30."]:before{transform: rotate(108deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 31."]:before{transform: rotate(111.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 32."]:before{transform: rotate(115.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 33."]:before{transform: rotate(118.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 34."]:before{transform: rotate(122.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 35."]:before{transform: rotate(126deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 36."]:before{transform: rotate(129.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 37."]:before{transform: rotate(133.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 38."]:before{transform: rotate(136.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 39."]:before{transform: rotate(140.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 40."]:before{transform: rotate(144deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 41."]:before{transform: rotate(147.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 42."]:before{transform: rotate(151.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 43."]:before{transform: rotate(154.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 44."]:before{transform: rotate(158.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 45."]:before{transform: rotate(162deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 46."]:before{transform: rotate(165.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 47."]:before{transform: rotate(169.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 48."]:before{transform: rotate(172.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 49."]:before{transform: rotate(176.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 50."]:before{transform: rotate(180deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 51."]:before{transform: rotate(183.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 52."]:before{transform: rotate(187.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 53."]:before{transform: rotate(190.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 54."]:before{transform: rotate(194.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 55."]:before{transform: rotate(198deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 56."]:before{transform: rotate(201.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 57."]:before{transform: rotate(205.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 58."]:before{transform: rotate(208.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 59."]:before{transform: rotate(212.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 60."]:before{transform: rotate(216deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 61."]:before{transform: rotate(219.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 62."]:before{transform: rotate(223.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 63."]:before{transform: rotate(226.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 64."]:before{transform: rotate(230.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 65."]:before{transform: rotate(234deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 66."]:before{transform: rotate(237.66deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 67."]:before{transform: rotate(241.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 68."]:before{transform: rotate(244.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 69."]:before{transform: rotate(248.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 70."]:before{transform: rotate(252deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 71."]:before{transform: rotate(255.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 72."]:before{transform: rotate(259.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 73."]:before{transform: rotate(262.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 74."]:before{transform: rotate(266.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 75."]:before{transform: rotate(27deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 76."]:before{transform: rotate(273.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 77."]:before{transform: rotate(277.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 78."]:before{transform: rotate(280.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 79."]:before{transform: rotate(284.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 80."]:before{transform: rotate(288deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 81."]:before{transform: rotate(291.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 82."]:before{transform: rotate(295.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 83."]:before{transform: rotate(298.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 84."]:before{transform: rotate(302.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 85."]:before{transform: rotate(306deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 86."]:before{transform: rotate(309.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 87."]:before{transform: rotate(313.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 88."]:before{transform: rotate(316.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 89."]:before{transform: rotate(320.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 90."]:before{transform: rotate(324deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 91."]:before{transform: rotate(327deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 92."]:before{transform: rotate(331.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 93."]:before{transform: rotate(334.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 94."]:before{transform: rotate(338.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 95."]:before{transform: rotate(342deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 96."]:before{transform: rotate(345.6deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 97."]:before{transform: rotate(349.2deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 98."]:before{transform: rotate(352.8deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 99."]:before{transform: rotate(356.4deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 100."]:before{transform: rotate(360deg)}
.c-lists-info .b-stats_bar .bar > div[style*="width: 51."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 52."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 53."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 54."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 55."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 56."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 57."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 58."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 59."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 60."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 61."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 62."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 63."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 64."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 65."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 66."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 67."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 68."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 69."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 70."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 71."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 72."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 73."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 74."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 75."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 76."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 77."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 78."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 79."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 80."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 81."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 82."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 83."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 84."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 85."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 86."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 87."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 88."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 89."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 90."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 91."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 92."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 93."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 94."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 95."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 96."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 97."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 98."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 99."]:after,
.c-lists-info .b-stats_bar .bar > div[style*="width: 100."]:after{
	transform: rotate(180deg);
}
.c-lists-info .b-stats_bar .bar > div[style*="width: 51."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 52."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 53."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 54."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 55."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 56."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 57."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 58."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 59."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 60."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 61."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 62."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 63."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 64."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 65."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 66."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 67."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 68."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 69."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 70."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 71."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 72."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 73."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 74."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 75."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 76."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 77."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 78."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 79."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 80."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 81."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 82."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 83."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 84."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 85."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 86."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 87."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 88."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 89."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 90."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 91."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 92."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 93."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 94."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 95."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 96."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 97."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 98."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 99."],
.c-lists-info .b-stats_bar .bar > div[style*="width: 100."]{
	clip: rect(auto, auto, auto, auto);
}
/*CIRCLE BAR:END*/

.p-profiles-show .profile-head:before {
  content: '';
  display: block;
  height: 300px; 
  background: url("https://images.alphacoders.com/175/thumb-1920-175151.jpg") no-repeat; 
  background-size: cover; 
  margin: -15px;
  margin-bottom: 5px; 
}
  
.p-profiles-show:before {
  content: " ";
  height: 100%;
  width: 100%;
  display: inline-block;
  position: fixed;
  background: url(https://i.pinimg.com/originals/52/b3/ca/52b3caaa9e283398b6d5b80a11938bed.gif) fixed;
}
```
