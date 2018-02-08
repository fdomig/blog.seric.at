---
author: Franziskus Domig
categories:
- Programming
date: 2008-03-12T22:59:00+00:00
tags:
- Algorithmus
- Bubblesort
- C
- Liste
title: Sortieren einer Liste mit C++
type: post
url: /2008/03/12/sortieren-einer-liste-mit-cpp/
---

Um eine (einfach) verkettete Liste mit C++ zu Sortieren gibt es unterschiedliche Ansätze. Ich habe die letzte Woche in einer Aufgabe im Rahmen meiner Algorithmik Vorlesung folgende Sortierungsfunktion implementiert, welche das Prinzip von [Bubblesort][1] verwendet. **Achtung**: Bubblesort ist ein Algorithmus, den man nicht in einer Anwendung verwenden solle. Bubblesort gehört mit  <img src="//s0.wp.com/latex.php?latex=O%28n%5E%7B2%7D%29+&#038;bg=ffffff&#038;fg=000&#038;s=0" alt="O(n^{2}) " title="O(n^{2}) " class="latex" />eine sehr schlechte [Laufzeit][2].
  
<!--more-->


  
Für die verkettete Liste habe ich folgende Struktur verwendet:

<pre lang="cpp">struct Node {
	int value;
	Node* pNext;
}</pre>

Die Funktion zum Sortieren der Liste sieht wie folgt aus. Als Parameter wird die Referenz auf den Pointer welcher auf den Anfang der Liste zeigt übergeben.

<pre lang="cpp">void sortList(Node*& pHead) {

	Node* pA = NULL;
	Node* pB = NULL;
	Node* pC = NULL;
	Node* pE = NULL;
	Node* pTmp = NULL;

	while (pE != pHead-&gt;pNext) {

		pC = pHead;
		pA = pHead;
		pB = pA-&gt;pNext;

		while (pA != pE) {
			if (pA-&gt;value &gt; pB-&gt;value) {
				if (pA == pHead) {
					pTmp = pB-&gt;pNext;
					pB-&gt;pNext = pA;
					pA-&gt;pNext = pTmp;
					pHead = pB;
					pC = pB;
				} else {
					pTmp = pB-&gt;pNext;
					pB-&gt;pNext = pA;
					pA-&gt;pNext = pTmp;
					pC-&gt;pNext = pB;
					pC = pB;
				}
			} else {
				pC = pA;
				pA = pA-&gt;pNext;
			}
			pB = pA-&gt;pNext;
			if (pB == pE)
				pE = pA;
		}
	}
}</pre>

 [1]: http://de.wikipedia.org/wiki/Bubblesort "Bubblesort - Wikipedia"
 [2]: http://de.wikipedia.org/wiki/Laufzeit_(Informatik)
