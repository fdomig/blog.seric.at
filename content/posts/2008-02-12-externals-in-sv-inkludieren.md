---
author: Franziskus Domig
categories:
- Programming
date: 2008-02-12T16:17:15+00:00
tags:
- Code
- Programming
- SVN
title: Externals in SVN inkludieren
type: post
url: /2008/02/12/externals-in-sv-inkludieren/
---

Weil wir gerade die Diskussion hatten wie man externe Repositories in das eigene Repository inkludieren kann, möchte ich dazu einige Zeilen tippen. Es manch manchmal durchaus externe Quellen wie zum für Beispiel eine Library oder Plugins und Themes in ein Projekt zu integrieren. Um dabei auch jeweils auf dem aktuellsten Stand zu bleiben, kann man mithilfe der SVN ([Subversion][1]) Eigenschaft &#8220;`externals`&#8221; ein externes Repository angeben.

Dazu macht man folgendes:<!--more-->

Zuerst importiert man in seine Working-Copy die externe Quelle mittels `svn checkout <url>`. Mit `svn propset svn:externals "<Verzeichnis> <url>" <Name>` wird nun die Eigenschaft des angegebenen Verzeichnis auf eine externe Quelle mit angegebener URI zum entsprechenden Repository gelegt. Nun kann das die Working-Copy mit `svn commit -m "added external ressource"` in das Repository importiert werden.

Um das ganze nun zu Überprüfen, reicht ein einfaches `svn update` und man sollte für das entsprechende Verzeichnis die Ausgabe: &#8220;`Fetching external item into <Name>`&#8221; zusätzlich zum Normalen Update-Text erhalten und das entsprechende Verzeichnis wird automatisch aus einem anderen Repository importiert bzw. aktualisiert.

Weiter [Informationen zur Thematik][2] gibt es außerdem beim svnbook.

 [1]: http://subversion.tigris.org
 [2]: http://svnbook.red-bean.com/en/1.0/ch07s03.html
