---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä nro 1
---

## Tehtävä 1: konvertoi celcius-asteet fahrenheiteiksi
Tehtävän alapuolella yleisiä ohjeita

<div id="P1-sortableTrash" class="sortable-code"></div> 
<div id="P1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function cToF(celsius) \n" +
    "{\n" +
    "  var cTemp = celsius;\n" +
    "  var cToFahr = cTemp * 9 / 5 + 32;\n" +
    "  var message = cTemp+'\xB0C is ' + cToFahr + ' \xB0F.';\n" +
    "  console.log(message);\n" +
    "} \\n cToF(60); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


# tenttitehtävien ratkaisun yleistä ohjeistusta
Muista sisennykset
Return lause voi olla keskellä funktiota, vaikka se yleensä on lopussa. Se katkaisee funktion suorituksen. 
Muuttujaa voi käyttää vasta sen jälkeen kun se on esitelty. 
Aloitussulkeella on aina lopetussulje. 

## parsons puzzlen käytön yleisohje 
Tehtävässä raahataan oikeaa koodia paikalleen ns. koodiblokkeina. Koodiblokki koostuu yhdestä tai useammasta koodirivistä. Se on vähän tarkka siitä mihin blokki raahataan. Joskus blokki saattaa mennä yli vasemmasta reunasta, mutta sen loppupään saa esiin kun vie hiiren koodiblokin päälle. 
Jos tila meinaa loppua kesken, käytä selaimen zoomaus-ominaisuutta. eri selaimissa eripaikoissa. Varmista että tiedät miten se toimii. 
## Tehtävien ratkaisuvinkkejä
Tehtävien ratkaisussa kannattaa kiinnittää huomiota muuttujien esittelyihin. Joskus kannattaa laittaa muuttujaesittelyt ensin ratkaisulaatikkoon. Voi myös lähteä liikkeelle kontrollirakenteiden (for, while, if, case) raahaamisella ratkaisulaatikkoon. 
Sitten kannattaa miettiä, miten niihin sijoitetaan arvoja ja mikä näyttää loogiselta järjestykseltä kun muuttujia käytetään eri vaiheissa ohjelmaa. 
Viimeisinä riveinä tehtävissä on yleensä console.log, vaikka voi se olla koodin seassakin. Useassa tehtävässä on mukana harhautuskoodirivejä, 
jotka kyllä huomaa muuttujien käytön perusteella. Niitä ei pidä raahata ratkaisulaatikkoon. 

AINA ei tarvitse alku-loppu-sulkeita: jos if "sisälle" tulee vain yksi rivi, usein jätetään aalto-sulkeet pois. Blokin sisällä näyttää usein olevan sisennysvirhe, 
mutta ajatelkaa että rivit ovat samalla tasolla.

tehtäviä voi yrittää niin monta kertaa kuin aikaa riittää. useasti hahmottamista helpottaa kun tekee sisennykset heti oikein. 
Kannattaa testata painamalla feedback-linkkiä. jos ohjelman kuvaus tuntuu hankalilta, kokeile päätellä, miten koodi järjestyy loogisesti. 

