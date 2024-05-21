# CRLFってなんぞ

CRとLFを合わせたもの

CR(=Carriage Return): 行頭回帰(=先頭へ戻る)  
LF(=Line Feed): 改行して、カーソルを新しい行に移動させる

したがって、CRLFとはカーソルを先頭に移動して次の行に改行する  

@正規表現  
CR: \r  
LF: \n  
CRLF: \r\n  

OSによって改行コードが異なる。  
LF: UNIX系  
CR: MacOSなど  
CRLF: Windowsなど  
