function autoForward() {
  var label = 'Forward';
  var recipient = 'forward to mail address here';  //add the recievers address
  var threads = GmailApp.search('label:' + label );
  for (var i = 0; i < threads.length; i++) {
    var messages = threads[i].getMessages();
    for (var j = 0; j < messages.length; j++) {
      messages[j].forward(recipient);
    }
  }
  var newLabel = GmailApp.getUserLabelByName("Forwarded"),
  oldLabel = GmailApp.getUserLabelByName("Forward"),
  threads1 = oldLabel.getThreads();
  for (var i = 0; i < threads1.length; i++) {
    threads1[i].addLabel(newLabel).removeLabel(oldLabel).refresh();
  }
}
