---
title: Programmieren mit der C-API in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
localization_priority: Normal
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 459e57d41ef7497c535e51944bbaf24daee84167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790562"
---
# <a name="programming-with-the-c-api-in-excel"></a>Programmieren mit der C-API in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Sie k�nnen das Microsoft Excel 2013 XLL Software Development Kit und die C-API verwenden, um hochleistungsf�hige Tabellenfunktionen f�r Excel 2013 zu erstellen. Die Upgrades auf die Excel 2013-C-API spiegeln den fortlaufenden Support f�r Benutzer wieder, f�r die die Leistung von Drittanbieterfunktionen oder internen Funktionen entscheidend ist.
  
## <a name="excel-programming-interfaces"></a>Excel-Programmierschnittstellen

Excel bietet mehrere Optionen f�r die Entwicklung von Anwendungen, die Schnittstellen damit bilden. Die Excel-Programmierschnittstellen wurden in fr�heren Versionen in der folgenden Reihenfolge hinzugef�gt:
  
- **XLM-Makrosprache:** Die erste Sprache f�r die Erweiterung von Excel, auf die vom Benutzer zugegriffen werden kann, und die Grundlage f�r die C-API. XLM wird zwar in Excel 2010 noch unterst�tzt, wurde aber schon lange durch Visual Basic for Applications (VBA) ersetzt. 
    
- **C-API und XLLs:** DLLs, die in Excel integriert sind. Diese DLLs bieten die direkteste und schnellste Schnittstele f�r das Hinzuf�gen von leistungsstarken Tabellenfunktionen, wenn auch zulasten der Komplexit�t im Vergleich zu sp�teren Technologien. 
    
- **VBA:** Visual Basic-Codeobjekte, die Excel-Arbeitsmappenobjekten zugeordnet sind. VBA erm�glicht das Auffangen von Ereignissen, die Anpassung und das Hinzuf�gen von benutzerdefinierten Funktionen und Befehlen. VBA ist die am weitesten verbreitete und am einfachsten verf�gbare Erweiterungsoption. 
    
- **COM:** Der Interoperabilit�tsstandard f�r Windows-basierte Anwendungen, �ber die Excel seine Ereignisse und Objekte verf�gbar macht. VBA verwendet COM zur Interaktion mit Excel. Excel exportiert COM-Typbibliotheken, die Sie bei der Erstellung von C++-COM-Coderessourcen und -Anwendungen unterst�tzen, die Excel extern steuern k�nnen. 
    
- **Microsoft .NET Framework:** Die mehrsprachiche verwaltete Codeumgebung, die f�r die schnelle Anwendungsentwicklung f�r verteilte Umgebungen konzipiert ist. Die prim�re Programmiersprache f�r Code, der auf .NET Framework basiert, ist C#, es k�nnen aber viele Sprachen in der Microsoft Intermediate Language (MSIL) kompiliert werden. Excel 2013 kann auf Coderessourcen zugreifen, die in .NET Framework-Assemblys enthalten sind. 
    
## <a name="when-to-use-the-c-api"></a>Anwendungsbereiche der C-API

Der Hauptgrund f�r das Schreiben von XLLs und die Verwendung der C-API ist die Erstellung von leistungsstarken Tabellenfunktionen. XLL-Funktionen werden zwar h�ufig als benutzerdefinierte Funktionen bezeichnet, aufgrund des Zeitaufwands, um sich das Verst�ndnis und die F�higkeiten anzueignen, die f�r das Schreiben von XLLs erforderlich sind, ist diese Technologie jedoch f�r die meisten Benutzer uninteressant. Nichtsdestotrotz bilden die Anwendungen mit leistungsstarken Funktionen und, in Excel 2013, die M�glichkeit, Multithread-Schnittstellen f�r leistungsstarke Serverressourcen zu schreiben, einen wichtigen Bestandteil der Excel-Erweiterbarkeit. 
  
Die Version der C-API, die in Excel 2007 eingef�hrt wurde, befasst sich in erster Linie mit den Aspekten im Zusammenhang mit leistungsstarken Berechnungen und nicht mit Features wie z. B. die Benutzeroberfl�che.
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>Schreiben von leistungsstarken benutzerdefinierten Tabellenfunktionen

Die Excel-C-API ist die ideal Wahl, wenn Sie leistungsstarke Tabellenfunktionen durch Erstellen von XLL-Add-Ins erstellen m�chten. Durch die C-API erhalten Sie den direktesten Zugriff auf Tabellendaten. Durch XLLs erh�lt Excel den direktesten Zugriff auf die DLL-Ressourcen. Die Leistung von XLLs wird in Excel 2013 durch Hinzuf�gen neuer Datentypen und vor allem die Unterst�tzung benutzerdefinierter Funktionen in grupppierten Servern weiter verbessert.
  
Das Arbeiten mit XLLs hat seinen Preis: Die C-API verf�gt nicht �ber die leistungsstarken Features zur schnellen Entwicklung von VBA, COM oder .NET Framework. Die Speicherverwaltung ist lediglich rudiment�r, weswegen mehr Verantwortung beim Entwickler liegt. Viele Excel-Features, die �ber COM durch VBA und .NET Framework verf�gbar sind, sind in der C-API nicht verf�gbar.
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>Zugreifen auf Multithread-Server mithilfe von XLL-Tabellenfunktionen

Mit der Multithread-Neuberechnung (MTR, Multithreaded Recalculation), die in Excel 2007 eingef�hrt wurde, k�nnen Sie threadsichere XLL-Tabellenfunktionen erstellen. Sie k�nnen diese Funktionen zum Zugreifen auf Multithread-Server verwenden. In sp�teren Abschniten wird ausf�hrlich beschrieben, wie dadurch die Leistung f�r den Benutzer erheblich gesteigert werden kann. F�r Excel-Benutzer, die manchmal Zugriff auf eine gro�e Menge Verarbeitungsleistung zugreifen m�ssen, bietet die Kombination einer XLL, die MTR und einen leistungsstarken Server f�r Berechnungen verwendet, die L�sung mit der h�chsten Leistung.
  
### <a name="customizing-the-excel-user-interface"></a>Anpassen der Excel-Benutzeroberfl�che

F�r viele Excel-Versionen war die C-API nicht die beste Wahl f�r das Anpassen der Benutzeroberfl�che. VBA verf�gt �ber hervorragenden Zugriff auf Excel-Objekte und -Ereignisse. Die in Excel 2007 eingef�hrte Benutzeroberfl�che in Excel 2007 unterscheidet sich sowohl im Hinblick auf das Aussehen und auch die zugrunde liegende Technologie erheblich von fr�heren Versionen. Sie k�nnen diese Schnittstelle am besten mithilfe von verwaltetem Coderessourcen anpassen.
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>Erstellen von Anwendungen, auf die im Internet zugegriffen werden kann

Excel Services, eingef�hrt mit dem 2007 Microsoft Office-System, bietet die beste M�glichkeit, um Benutzern mithilfe von standardm��igen Webbrowsertools Zugriff auf Arbeitsmappen und Excel-Funktionen zu gew�hren. Zusammen mit .NET Framework-Entwicklungssprachen und -ressourcen, stellen diese Technologien in Zukunft einen wichtigen Bestandteil der Excel-Bereitstellung f�r Benutzer dar.
  
### <a name="controlling-excel-from-external-applications"></a>Steuern von Excel aus externen Anwendungen

Excel macht seine Objekte, Methoden und Ereignisse �ber die COM-Schnittstelle verf�gbar. Sie k�nnen COM daher zum Erstellen von eigenst�ndigen Anwendungen verwenden, die eine Excel-Sitzung starten und steuern bzw. eine vorhandene Excel-Sitzung steuern k�nnen. Sie k�nnen in unterschiedlichen Entwicklungssprachen, einschlie�lich C++ und VBA auf die �ber COM verf�gbar gemachte Excel-Benutzeroberfl�che zugreifen. C# und das .NET Framework bietet auf �hnliche Weise eine Schnittstelle zu Excel, die den Remotezugriff auf und die Steuerung von Excel erm�glicht.
  
## <a name="asynchronous-calling-of-excel"></a>Asynchrones Aufrufen von Excel

In Excel k�nnen XLLs die C-API nur aufrufen, wenn Excel die Steuerung an die XLL �bergeben hat. Eine Tabellenfunktion, die von Excel aufgerufen wird, kann Excel mithilfe der C-API zur�ckrufen. Ein XLL-Befehl, der von Excel aufgerufen wird, kann die C-API aufrufen. DLL- und XLL-Funktionen und Befehle, die von VBA aufgerufen, wenn VBA wiederum selbst von Excel aufgerufen wurde, k�nnen die C-API aufrufen. Sie k�nnen beispielsweise keinen zeitlich festgelegten Windows-R�ckruf in XLL festlegen und die C-API von dort aufrufen, und Sie k�nnen die C-API nicht von einem Hintergrundthread aufrufen, der von XLL erstellt wurde. Das asynchrone Aufrufen von Excel mithilfe von Com von einer DLL- oder XLL-Funktion aus wird nicht empfohlen.
  
Dies ist sehr einschr�nkend, denn es gibt m�glicherweise Anwendungen, in denen Sie m�chten, dass Excel auf ein Ereignis asnychron reagiert. Vielleicht m�chten Sie beispielsweise, dass Excel ein Datenst�ck im Internet abruft und erneut berechnet, wenn sich die Daten �ndern. Oder Sie m�chten, dass ein Hintergrundthread eine Berechnung ausf�hrt und Excel diese nach Abschluss neu berechnet.
  
Sie erreichen dies, indem Sie Excel aktiv �nderungen abfragen lassen, dies ist ineffizient ist und einschr�nkend, da Excel dabei h�ufig seine normale Aktivit�t unterbrechen muss. Sie k�nnen zwar mithilfe der C-API oder VBA einen wiederholten zeitgesteuerten Befehl einrichten, dies ist aber keine ideale L�sung.
  
Im Idealfall ben�tigen Sie einen effizienteren externen Prozess, der nach der �nderung von Daten sucht, und dieser externe Prozess soll ausl�sen, dass Excel das Update abruft und eine Neuberechnung durchf�hrt. Hierf�r k�nnen Sie eine Anwendung verwenden, die �ber COM eine Schnittstelle mit Excel bildet. COM ist nicht wie die C-API darauf beschr�nkt, nur dann Aufrufen zu t�tigen, wenn Excel seine Steuerung ausdr�cklich �bergeben hat. COM-Anwendungen k�nnen Excel-Methoden aufrufen, wenn Excel den Status "Bereit" aufweist, diese Methodenaufrufe werden jedoch m�glicherweise ignoriert, wenn Dialogfelder angezeigt werden, Men�s abgerufen werden oder wenn ein Makro ausgef�hrt wird.
  
## <a name="c-api-and-its-relation-to-xlm"></a>Die C-API und ihre Beziehung zu XLM

Die Excel-Makrosprache (XLM) war die erste Programmierumgebung in Excel, auf die der Benutzer zugreifen konnte. Mit dieser Sprache konnten Benutzer benutzerdefinierte Befehle und Funktionen in speziellen Makrovorlagen erstellen, die wie normale Arbeitsbl�tter aussehen. XLM-Makrovorlagen werden in Excel 2013 immer noch unterst�tzt. Zus�tzlich zu den folgenden Elementen, die in einem Arbeitsblatt nicht eingegeben werden k�nnen, k�nnenSie alle gew�hnlichen Tabellenblattfunktion wie **SUM** und **LOG** in einer Makrovorlage verwenden: 
  
- Funktionen f�r Arbeitsbereichsinformationen wie **GET.CELL** und **GET.WORKBOOK**.
    
- Funktionen, die Befehlen entsprechen, die eine Automatisierung gew�hnlicher Benutzervorg�nge erm�glichen, z. B. **DEFINE.NAME** und **PASTE**.
    
- Funktionen, die im Zusammenhang mit Add-Ins stehen, z. B. **REGISTER**.
    
- Ereignistraps, die Befehlen entsprechen, z. B. **ON.ENRTY** und **ON.TIME**.
    
- Makrofunktionsspezifische Operationen wie **ARGUMENT** und **VOLATILE**.
    
- Flusssteuerungsoperationen wie **GOTO** und **RETURN**.
    
In Excel, Version 3, gab es eine einschr�nkte Version der C-API. In Excel, Version 4, wurde die XLM-Sprache jedoch der C-API zugeordnet. Seitdem k�nnen DLLs alle Tabellenblattfunktionen, Funktionen f�r Makrovorlageninformationen und Befehle aufrufen und Ereignistraps festlegen. DLLs k�nnen aus der C-API heraus keine XLM-Flusssteuerungsfunktionen aufrufen. Diese Makrovorlagenfunktionen und Befehle sind in der Hilfedatei "XLMacr8.hlp" (bisher bezeichnet als "Macrofun.hlp") dokumentiert. Um diese Hilfedatei abzurufen, rufen Sie das [Microsoft Download Center](http://download.microsoft.com) auf, und suchen Sie nach "XLMacr8.hlp". 
  
> [!NOTE]
> [!HINWEIS] In Windows Vista und Windows 7 werden HLP-Dateien nicht direkt unterst�tzt, Sie k�nnen aber das [Windows-Hilfeprogramm (WinHlp32.exe) f�r Windows Vista](http://go.microsoft.com/fwlink/?LinkID=82148) oder das [Windows-Hilfeprogramm (WinHlp32.exe) f�r Windows 7](http://www.microsoft.com/download/en/details.aspx?id=91) von Microsoft herunterladen und die Dateien damit �ffnen. 
  
DLLs rufen C-API-Entsprechungen dieser Funktionen und Befehle mithilfe der R�ckruffunktionen **Excel4**, **Excel4v**, **Excel12** und **Excel12v** auf (die beiden letzten wurden in Excel 2007 eingef�hrt). Aufgez�hlte Konstanten, die den einzelnen Funktionen und Befehlen entsprechen, sind in einer Headerdatei definiert und werdenals eines der Argumente an diese R�ckrufe �bergeben. **GET.CELL** wird beispielsweise durch **xlfGetCell**, **REGISTER** durch **xlfRegister** und **DEFINE.NAME** durch **xlcDefineName** dargestellt.
  
Abgesehen davon, dass die Tabellenblattfunktionen und Makrovorlagenfunktionen und Befehle bereitgestellt werden, liefert die C-API Funktions- und Befehlsaufz�hlungen, die nur mithilfe dieser R�ckrufe innerhalb einer DLL aufgerufen werden k�nnen. Mit **xlGetName** kann eine DLL beispielsweise ihren eigenen vollst�ndigen Pfad und Dateinamen ermitteln, der f�r die Registrierung von Funktionen und Befehlen bei Excel erforderlich ist. 
  
Seit der Einf�hrung von VBA-Bl�ttern (Visual Basic for Applications) in Excel, Version 5, und des Visual Basic-Editors (VBE) in Version 8 (Excel 97), besteht die einfachste M�glichkeit f�r Benutzer zum Anpassen von Excel darin, VBA anstele von XLM zu verwenden. Daher ist ein Gro�teil der neuen Funktionalit�t, die in sp�teren Verseionen von Excel eingef�hrt wurde, �ber VBA, jedoch nicht �ber XLM oder die C-API verf�gbar.
  
Weitere Informationen finden Sie unter [Was ist neu in der C-API f�r Excel 2013](what-s-new-in-the-c-api-for-excel.md).
  
## <a name="see-also"></a>Siehe auch



[Was ist neu in der C-API f�r Excel 2013](what-s-new-in-the-c-api-for-excel.md)
  
[C-API-R�ckruf funktioniert Excel4 Excel12](c-api-callback-functions-excel4-excel12.md)


[Erste Schritte mit Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

