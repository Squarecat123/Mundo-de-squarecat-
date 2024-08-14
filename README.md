function onOpen() {
  var ui = SpreadsheetApp.getUi();
  ui.createMenu('Tá cansado?')
      .addItem('Verificar Cansaço', 'verificarCansado')
      .addToUi();
}

function verificarCansado() {
  var ui = SpreadsheetApp.getUi();
  var resposta = ui.prompt('Você está cansado? (Digite "sim" ou "não")');
  
  var respostaUsuario = resposta.getResponseText().toLowerCase();
  
  if (respostaUsuario === 'sim') {
    ui.alert('Descanso é importante! Tire um tempo para relaxar.');
  } else if (respostaUsuario === 'não') {
    ui.alert('Ótimo! Continue com sua produtividade.');
  } else {
    ui.alert('Resposta inválida. Digite "sim" ou "não".');
  }
}
