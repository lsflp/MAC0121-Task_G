TAREFA G
========

## Geral

- [x] Colocar o gabarito (EM TODOS OS ARQUIVOS).
- [x] Tirar tabs.
- [x] Checar indentação.
- [x] Checar codificação (em todos os arquivos).
- [x] Checar espaços antes de abre chaves e parênteses.
- [ ] Descrever o programa no início.
- [x] Deixar em 65 colunas.
- [x] Colocar as funções de cada biblioteca na frente dos includes.
- [ ] Comentar cada função.
- [x] Ultima linha com newline.

## ordenacao.c

- Módulo que contém a biblioteca de ordenação.
- Implementação deve ser igual às notas de aula.
- Os protótipos não são iguais, então deve ter uma função-embrulho pública que ordena o vetor 0...n-1, com o seguinte protótipo:
	void nome_da_funcao (int *v, int n);
- Usar static para impedir a visualização das funções "de verdade".
- A documentação deve conter, além das informações, informações sobre o consumo de tempo.

	### inserctionsort

	- http://www.ime.usp.br/~pf/algoritmos/aulas/ordena.html
	- [x] Função embrulho pública: void inserctionsort (int *v, int n);
	- [x] Função privada: static void inserctionsrt (int *v, int n).

	### mergesort

	http://www.ime.usp.br/~pf/algoritmos/aulas/mrgsrt.html
	- [x] Função embrulho pública: void mergesort (int *v, int n);
	- [x] Função privada: static void mergesrt (int p, int r, int v[]);
		No caso, chamar em mergesort: mergesrt (0, n, *v).
	- [x] Deve ter a função intercala:
		static void intercala (int p, int q, int r, int v[]);, onde:
			p é o início do vetor.
			q é o meio.
			r é o final.

	### quicksort

	http://www.ime.usp.br/~pf/algoritmos/aulas/quick.html
	- [x] Função embrulho pública: void quicksort (int *v, int n);
	- [x] Função privada: static void quicksrt (int *v, int p, int r)
		No caso, chamar em quicksort: quicksrt (v, 0, n-1).
	- [x] Deve ter a função separa:
		static int separa (int v[], int p, int r), onde:
			p é o início do vetor.
			q é o meio.
			r é o final.
		que devolve um elemento j do conjunto p..r tal que
			v[p..j-1] <= v[j] < v[j+1..r] .		

	### heapsort

	http://www.ime.usp.br/~pf/algoritmos/aulas/hpsrt.html
	- [x] Função embrulho pública: void heapsort (int *v, int n);
	- [x] Função privada: static void heapsrt (int *v, int n).
		No caso, o vetor vai de 1...n.
	- [x] Deve ter a função peneira:
		static void peneira (int p, int m, int v[]).
	- [x] Descobrir quais são os argumentos corretos.

## ordenacao.h

- Arquivo interface de ordenacao.c

## testaordenacao.c

- Módulo de teste das ordenações.

- [x] Fazer uma função que gere um vetor com 40000 números aleatórios.
- [x] Ordenar o vetor.
- [x] Verificar se está em ordem.
