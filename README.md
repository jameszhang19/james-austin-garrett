# james-austin-garrett

var answer = [];
var score = 0;
var improvement = "";
onEvent("startbutton", "click", function( ) {
  setScreen("Q1");
});
onEvent("Q1Yes", "click", function( ) {
  setScreen("Q2");
  appendItem(answer, "Yes");
  score = score + 2;
});
onEvent("Q1No", "click", function( ) {
  setScreen("Q2");
  appendItem(answer, "No");
  improvement = "Have breakfast every day";
});
onEvent("Q2Yes", "click", function( ) {
  setScreen("Q3");
  appendItem(answer, "Yes");
  score = score + 2;
});
onEvent("Q2No", "click", function( ) {
  setScreen("Q3");
  appendItem(answer, "No");
  improvement = improvement + ", slow down when having meals";
});
onEvent("Q3Yes", "click", function( ) {
  setScreen("Q4");
  appendItem(answer, "Yes");
  score = score + 2;
});
onEvent("Q3No", "click", function( ) {
  setScreen("Q4");
  appendItem(answer, "No");
  improvement = improvement + ", sit straight when reading or watching videos";
});
onEvent("Q4Yes", "click", function( ) {
  setScreen("Q5");
  appendItem(answer, "Yes");
  score = score + 2;
});
onEvent("Q4No", "click", function( ) {
  setScreen("Q5");
  appendItem(answer, "No");
  improvement = improvement + ", do some exercise outdoor everyday";
});
onEvent("Q5Yes", "click", function( ) {
  setScreen("Report");
  appendItem(answer, "Yes");
  score = score + 2;
  if (improvement == "") {
    setText("reportText", "Score: " + score + "/10" + "\n" + "improvement: " + "none, your habits are good !");
  } else {
    setText("reportText", "Score: " + score + "/10" + "\n" + "improvement: " + improvement);
  }
});
onEvent("Q5No", "click", function( ) {
  setScreen("Report");
  appendItem(answer, "No");
  improvement = improvement + ", sit properly and do not cross your legs";
  setText("reportText", "Score: " + score + "/10" + "\n" + "improvement: " + improvement);
});
