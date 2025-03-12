## Exercício 4

```
@Test(expected = java.util.EmptyStackException.class)
public void testEmptyStackException() {
	Stack s<Integer> = new Stack<Integer>();
	int r = stack.pop();
}
```
## Exercício 5

```
 @Test
public void testEmptyArray(){
	List<Integer> s = new ArrayList<Integer>();
	bool empty = s.isEmpty();
	assertTrue(s);
}


 @Test
public void testNonEmptyArray(){
	List<Integer> s = new ArrayList<Integer>();
	s.add(1);
	bool empty = s.isEmpty();
	assertFalse(s);
}

 @Test
public void testSizeArray(){
	List<Integer> s = new ArrayList<Integer>();
	s.add(1);
   	s.add(2);
    	s.add(3);
    	int size = s.size();
    	int first = s.get(0);
    	int second = s.get(1);
    	int thrid = s.get(2);
    	assertEqual(tamanho, 3);
    	assertEqual(first, 1);
    	assertEqual(second, 2);
    	assertEqual(third, 3);
}

 (Cansei)
```
 
 Exercício 6
 
 Chamada 		Cob Comandos 	Cobertura Branches
 
 f(0,0)			1		1
 
 f(1,1)			4		1
 
 f(0,0) e f(1,1)	4		2

| Chamada         | Cobertura Comandos | Cobertura Branches |
| --------------- | ------------------ | ------------------ |
| f(0,0)          | 1                  | 1                  |
| f(1,1)          | 4                  | 1                  |
| f(0,0) e f(1,1) | 4                  | 2                  |

 
 
 Exercício 7
 
 a. O teste erra se a nota do aluno é exatamente 90
 b. Cobertura comandos 100% e de branches 100%.
 c. Não, os testes percorrem todos os comandos, mas são rasos.
 Não checam todas as classes de equivalência do conjunto de entrada.
 
Exercício 8

```
 assertEquals(list.size(), 10);
 
 assertEquals(result , "Engenharia Software");
```

 Exercício 9
 
 B pode ser uma API que é chamada por A.
 B' é o mock desssa API, que por erro do programador,
 faz um retorno de requisição de um arquivo JSON com nomes de atributos diferente da API B em si.
 Assim, o teste unitário passa, mas de integração não.
 