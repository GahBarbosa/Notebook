Node.js® é um cross platform [[Runtime Environment]] JavaScript e [[Open-source]].

O Node permite que os desenvolvedores escrevam código JavaScript que é executado diretamente em um processo de computador em vez de em um navegador. O Node pode, portanto, ser usado para escrever aplicativos do lado do servidor com acesso ao sistema operacional, sistema de arquivos e tudo mais necessário para construir aplicativos totalmente funcionais.

Node.js é escrito em [[C]], [[C++]] e [[JavaScript]] e é construído no mecanismo [[JavaScript V8]]  de código aberto que também alimenta JS em navegadores. Como o V8 oferece suporte a novos recursos em [[JavaScript]], eles são incorporados ao Node.

Feito com a [[Arquitetura Orientada a Eventos]] e [[Assíncrono]]. Na prática, isso significa que o Node foi desenvolvido bem para lidar com código JavaScript para realizar muitas atividades ao mesmo tempo sendo assim [[Multithreading]], como leitura e gravação no sistema de arquivos, manipulação de conexões com servidores de banco de dados ou manipulação de solicitações como um servidor web.

Para lidar com código assíncrono, o Node usa um sistema baseado em [[Dev/Conceitos/Callback|Callback]]. As funções e métodos que implementarão alguma atividade assíncrona recebem uma função [[Callback]]. Este callback será chamado sempre que a operação assíncrona for resolvida. 

#### Bibliotecas:
	[[Express]]

#### A aprender:
	[[Nest.js]]