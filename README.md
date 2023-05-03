def enforcado():
    if num_erros < 6:
        return False
    else:
        return True    

def codifica(palavra):
    resp = ""
    for c in palavra:
        resp = resp + "_ "
    return resp    

def acertou(pal):
    if "_" in pal:
        return False
    else:
        return True

def chuta(secret, word, letter):
    i = 0
    resp = ""
    while i < len(word):
        if word[i] == letter:     
            resp = resp + lette + ""
        else:
            resp = resp + secret [2*i] + ""
   i = i + 1
   return resp   

palavra = "girafa"
num_erros = 0
segredo = codifica(palavra)

while not enforcado(num_erros) and not acertou():
   #imprime a tela do jogo
   prints(segredo)
   print(" erros: ", num_erros)

   #pede para usuario digitar letra

   Letra = input ("Informe uma letra: ")

   #atualiza jogo com a letra digitada
   if not Letra in palavra:
        num_erros = num_erros + 1
    else:
        segredo = chuta(segredo, palavra, Letra) 
