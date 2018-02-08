---
author: Franziskus Domig
categories:
- Programming
date: 2008-02-08T11:19:46+00:00
tags:
- C
- Programming
- Rekursion
- Source
- Türme von Hanoi
title: Die Türme von Hanoi in C
type: post
url: /2008/02/08/die-turme-von-hanoi-in-c/
---

Ein beliebtes Beispiel für rekursives Programmieren ist das 1883 vom Mathematiker Eduard Lucas erfundene (Mathematik-)Denkspiel &#8220;[Die Türme von Hanoi][1]&#8220;.

Das Spiel besteht darin, einen Stapel A von verschieden großen Scheiben, welche der Größe nach sortiert sind, auf einen Stapel C mithilfe eines &#8220;Zwischenlager&#8221;-Stapel B zu bewegen ohne dabei eine größere Scheibe auf eine kleinere Scheibe zu legen. Am Ende muss auf dem Stapel C die selbe geordnete Reihenfolge vorliegen, wie auf dem Ursprungs-Stapel A. Zusätzlich gilt, dass jeweils nur eine Scheibe bewegt werden darf.

Der Stapel A mit 4 Scheiben wird so gelöst:

<img src="/uploads/2008/02/tower_of_hanoi_4.gif" rel="attachment wp-att-10" alt="Türme von Hanoi" title="Türme von Hanoi (4 Scheiben)" class="align-none" height="125" width="320" />

Dazu gibt es nun einen rekursiven Lösungsweg in der Programmierung. Man löst jeweils das kleinste Problem und wendet das selbe auf das nächt größere Problem an. Das heißt, man löst das Problem eines Stapels mit zwei Scheiben, kann dieses Problem gelöst werden, löst man das Problem für 2+1 bzw. schlussendlich n+1 Scheiben.

Der entsprechende Algorithmus in C:

<pre lang="c">void hanoi(int h, char src, char dest, char tmp) {
    if (h == 1) {
        moveDisk(src, dest);
    } else {
        hanoi(h-1, src, tmp, dest);
        moveDisk(src, dest);
        hanoi(h-1, tmp, dest, src);
    }
}

void moveDisk(char src, char dest) {
    printf("Move %c to %c\n", src, dest);
}</pre>

(Als simples Beispiel wird moveDisk() lediglich die entsprechenden Züge ausgeben.)

 [1]: http://de.wikipedia.org/wiki/T%C3%BCrme_von_Hanoi
