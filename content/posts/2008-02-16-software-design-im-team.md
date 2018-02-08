---
author: Franziskus Domig
categories:
- Programming
date: 2008-02-16T17:26:05+00:00
tags:
- Collaboration
- Design
- Planung
- Software
- Team
title: Software Design im Team
type: post
url: /2008/02/16/software-design-im-team/
---

Leider scheitern viele innovative (Software) Projekte und Ideen an der Umsetzung. Oftmals kommen Programmierer mit verschiedenen Kenntnissen sowie Erwartungen zu dem Projekt. Es gibt selten ein Team mit den gleichen Kenntnissen der entsprechenden Programmiersprache sowie der selben Art an die unterschiedlichen Probleme heranzutreten und vorzugehen.

Hier möchte ich einige aus meiner Sicht essentiellen Punkte erläutern, welche einer guten Idee auch zu einer entsprechend guten Umsetzung verhelfen. Das ganze werde ich in meheren Teilen veröffentlichen und starte heute mit Teil 1:<!--more-->

### Teil 1: Planung

Wie ich finde gehört ein neues Projekt ausführlich geplant. Einfach drauflos zu programmieren wird in den meisten Fällen nicht zum Erfolg führen und vielleicht zwar zu einer benutzbaren aber nicht durchdachten Software führen. Dazu müssen einige Punkte beachtet werden.

  1. **Erweiterbarkeit**
  
    Das Produkt muss einfach erweiterbar sowie sollte keine gravierenden Änderungen am ursprünglichen Code verlangen. Zusätzlich sollten Änderungen keine Auswirkungen auf die Umgebung in welcher die Software verwendet wird benötigen. (Abgesehen von Erweiterungen, welche z.B. ein zusätzliches Protokoll bzw. eine zusätzliche Funktionalität bieten ohne, dass dabei die ursprüngliche Funktionalität beeinträchtigt wird).
  2. **Robustheit**
  
    Die Software sollte soweit durchdacht sein, dass diese unter enormen Belastungen wie zum Beispiel mit geringem verfügbaren Hauptspeicher oder trotz hoher Prozessorlast vernünftig arbeitet.
  3. **Sicherheit**
  
    Trotz etwaigen böswilligen Attacken und Einflüsse sollte die Software standhalten und fehlerfrei arbeiten und reagieren.
  4. **Wartbarkeit**
  
    Das Programm kann innerhalb eines definierten Zeitraums gewartet werden. Dazu zählen insbesondere Updates von Bibliotheken oder auch das eventuelle Beseitigen von Fehlern.
  5. **Kompatibilität**
  
    Wenn möglich sollte eine neue Software kompatibel zu bereits bestehenden Lösungen sein und vor allem mit anderen Produkten zusammenarbeiten können. Dazu zählt auch die Abwärtskompatibilität zu der (zumindest) jeweils vorhergehenden Version der Software.
  6. **Modularisierung**
  
    Ein sehr wichtiger Punkt beim Arbeiten (bzw. Programmieren) im Team ist es, dass zusammengehörende Code-Teile auch zusammengefasst und ausgelagert werden. Dies führt auch gleich zu einer besseren Wartbarkeit und ermöglicht es im Team an unterschiedlichen Code-Teilen bzw. Modulen gleichzeitig zu arbeiten.
  7. **Wiederverwendbarkeit**
  
    Auch wenn die zu erstellende Software nur für den einfachen Einsatz konzipiert wird kann es durchaus der Fall sein, dass die selbe Software (eventuell adaptiert) bei einem anderen Projekt wiederverwendet werden sollte. Ein Projektteam sollte deswegen dies bereits bei der Erstellung des Projektes mitberücksichtigen.

Demnächst folgt der zweite Teil hier bei seric.at.
