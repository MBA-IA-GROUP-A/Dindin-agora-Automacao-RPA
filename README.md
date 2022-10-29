# Projeto de automação de processo com UiPath Studio

## Passo a passo

1. Começar com o ```Excel Process Scrope```

2. ```Use Excel File``` para ler o arquivo ```money.xlsx``` que contém as moedas disponiveis para conversão e os valores a serem convertidos

3. Usar um ```For Each Excel Row```

4. Salvar o valor de cada interação da coluna ```Symbol``` em uma variavel chamada ```coin``` com o ```Read Cell Value```

5. Abrir o navegador com o ```Use Browser Chrome```

6. Navegar até ```google.com``` com o ```Go To URL```

7. Escrever na barra de busca do Google, utilizando o ```Type into 'INPUT'```. O text escrito é ```coin + " to BRL" + "[k(enter)]"```

8. Ler na tela com o ```Get Text```, o valor da conversão e salvar em uma variavel ```currentBRL```

9. Novamente usar o ```For Each Excel Sheet```

10. Com o ```Write Cell``` escrever na coluna ```Converseio``` o valor da variavel ```currentBRL```

11. Com o ```Read Cell Value``` pegar o valor da coluna ```Tax per currency``` e salvar em uma variavel ```tax```

12. Com o ```Read Cell Value``` pegar o valor da coluna ```Price to convert``` e salvar em uma variavel ```currentVar```

13. Com o ```Write Cell``` multiplicar o ```currentVar``` com o ```currentBRL```, para ter o valor convertido sem taxa, e salvar na coluna ```Price converted```

14. Com o ```Write Cell``` multiplicar os valores ```currentVar```, ```currentBRL``` e ```tax + 1```, para ter o valor convertido com taxa, e salvar na coluna ```Price with tax```

15. Fim