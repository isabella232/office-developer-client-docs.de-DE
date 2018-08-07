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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 459e57d41ef7497c535e51944bbaf24daee84167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790562"
---
# <a name="programming-with-the-c-api-in-excel"></a>Programmieren mit der C-API in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Sie können das Microsoft Excel 2013 XLL Software Development Kit und die C-API verwenden, um hochleistungsfähige Tabellenfunktionen für Excel 2013 zu erstellen. Die Upgrades auf die Excel 2013-C-API spiegeln den fortlaufenden Support für Benutzer wieder, für die die Leistung von Drittanbieterfunktionen oder internen Funktionen entscheidend ist.
  
## <a name="excel-programming-interfaces"></a>Excel-Programmierschnittstellen

Excel bietet mehrere Optionen für die Entwicklung von Anwendungen, die Schnittstellen damit bilden. Die Excel-Programmierschnittstellen wurden in früheren Versionen in der folgenden Reihenfolge hinzugefügt:
  
- **XLM-Makrosprache:** Die erste Sprache für die Erweiterung von Excel, auf die vom Benutzer zugegriffen werden kann, und die Grundlage für die C-API. XLM wird zwar in Excel 2010 noch unterstützt, wurde aber schon lange durch Visual Basic for Applications (VBA) ersetzt. 
    
- **C-API und XLLs:** DLLs, die in Excel integriert sind. Diese DLLs bieten die direkteste und schnellste Schnittstele für das Hinzufügen von leistungsstarken Tabellenfunktionen, wenn auch zulasten der Komplexität im Vergleich zu späteren Technologien. 
    
- **VBA:** Visual Basic-Codeobjekte, die Excel-Arbeitsmappenobjekten zugeordnet sind. VBA ermöglicht das Auffangen von Ereignissen, die Anpassung und das Hinzufügen von benutzerdefinierten Funktionen und Befehlen. VBA ist die am weitesten verbreitete und am einfachsten verfügbare Erweiterungsoption. 
    
- **COM:** Der Interoperabilitätsstandard für Windows-basierte Anwendungen, über die Excel seine Ereignisse und Objekte verfügbar macht. VBA verwendet COM zur Interaktion mit Excel. Excel exportiert COM-Typbibliotheken, die Sie bei der Erstellung von C++-COM-Coderessourcen und -Anwendungen unterstützen, die Excel extern steuern können. 
    
- **Microsoft .NET Framework:** Die mehrsprachiche verwaltete Codeumgebung, die für die schnelle Anwendungsentwicklung für verteilte Umgebungen konzipiert ist. Die primäre Programmiersprache für Code, der auf .NET Framework basiert, ist C#, es können aber viele Sprachen in der Microsoft Intermediate Language (MSIL) kompiliert werden. Excel 2013 kann auf Coderessourcen zugreifen, die in .NET Framework-Assemblys enthalten sind. 
    
## <a name="when-to-use-the-c-api"></a>Anwendungsbereiche der C-API

Der Hauptgrund für das Schreiben von XLLs und die Verwendung der C-API ist die Erstellung von leistungsstarken Tabellenfunktionen. XLL-Funktionen werden zwar häufig als benutzerdefinierte Funktionen bezeichnet, aufgrund des Zeitaufwands, um sich das Verständnis und die Fähigkeiten anzueignen, die für das Schreiben von XLLs erforderlich sind, ist diese Technologie jedoch für die meisten Benutzer uninteressant. Nichtsdestotrotz bilden die Anwendungen mit leistungsstarken Funktionen und, in Excel 2013, die Möglichkeit, Multithread-Schnittstellen für leistungsstarke Serverressourcen zu schreiben, einen wichtigen Bestandteil der Excel-Erweiterbarkeit. 
  
Die Version der C-API, die in Excel 2007 eingeführt wurde, befasst sich in erster Linie mit den Aspekten im Zusammenhang mit leistungsstarken Berechnungen und nicht mit Features wie z. B. die Benutzeroberfläche.
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>Schreiben von leistungsstarken benutzerdefinierten Tabellenfunktionen

Die Excel-C-API ist die ideal Wahl, wenn Sie leistungsstarke Tabellenfunktionen durch Erstellen von XLL-Add-Ins erstellen möchten. Durch die C-API erhalten Sie den direktesten Zugriff auf Tabellendaten. Durch XLLs erhält Excel den direktesten Zugriff auf die DLL-Ressourcen. Die Leistung von XLLs wird in Excel 2013 durch Hinzufügen neuer Datentypen und vor allem die Unterstützung benutzerdefinierter Funktionen in grupppierten Servern weiter verbessert.
  
Das Arbeiten mit XLLs hat seinen Preis: Die C-API verfügt nicht über die leistungsstarken Features zur schnellen Entwicklung von VBA, COM oder .NET Framework. Die Speicherverwaltung ist lediglich rudimentär, weswegen mehr Verantwortung beim Entwickler liegt. Viele Excel-Features, die über COM durch VBA und .NET Framework verfügbar sind, sind in der C-API nicht verfügbar.
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>Zugreifen auf Multithread-Server mithilfe von XLL-Tabellenfunktionen

Mit der Multithread-Neuberechnung (MTR, Multithreaded Recalculation), die in Excel 2007 eingeführt wurde, können Sie threadsichere XLL-Tabellenfunktionen erstellen. Sie können diese Funktionen zum Zugreifen auf Multithread-Server verwenden. In späteren Abschniten wird ausführlich beschrieben, wie dadurch die Leistung für den Benutzer erheblich gesteigert werden kann. Für Excel-Benutzer, die manchmal Zugriff auf eine große Menge Verarbeitungsleistung zugreifen müssen, bietet die Kombination einer XLL, die MTR und einen leistungsstarken Server für Berechnungen verwendet, die Lösung mit der höchsten Leistung.
  
### <a name="customizing-the-excel-user-interface"></a>Anpassen der Excel-Benutzeroberfläche

Für viele Excel-Versionen war die C-API nicht die beste Wahl für das Anpassen der Benutzeroberfläche. VBA verfügt über hervorragenden Zugriff auf Excel-Objekte und -Ereignisse. Die in Excel 2007 eingeführte Benutzeroberfläche in Excel 2007 unterscheidet sich sowohl im Hinblick auf das Aussehen und auch die zugrunde liegende Technologie erheblich von früheren Versionen. Sie können diese Schnittstelle am besten mithilfe von verwaltetem Coderessourcen anpassen.
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>Erstellen von Anwendungen, auf die im Internet zugegriffen werden kann

Excel Services, eingeführt mit dem 2007 Microsoft Office-System, bietet die beste Möglichkeit, um Benutzern mithilfe von standardmäßigen Webbrowsertools Zugriff auf Arbeitsmappen und Excel-Funktionen zu gewähren. Zusammen mit .NET Framework-Entwicklungssprachen und -ressourcen, stellen diese Technologien in Zukunft einen wichtigen Bestandteil der Excel-Bereitstellung für Benutzer dar.
  
### <a name="controlling-excel-from-external-applications"></a>Steuern von Excel aus externen Anwendungen

Excel macht seine Objekte, Methoden und Ereignisse über die COM-Schnittstelle verfügbar. Sie können COM daher zum Erstellen von eigenständigen Anwendungen verwenden, die eine Excel-Sitzung starten und steuern bzw. eine vorhandene Excel-Sitzung steuern können. Sie können in unterschiedlichen Entwicklungssprachen, einschließlich C++ und VBA auf die über COM verfügbar gemachte Excel-Benutzeroberfläche zugreifen. C# und das .NET Framework bietet auf ähnliche Weise eine Schnittstelle zu Excel, die den Remotezugriff auf und die Steuerung von Excel ermöglicht.
  
## <a name="asynchronous-calling-of-excel"></a>Asynchrones Aufrufen von Excel

In Excel können XLLs die C-API nur aufrufen, wenn Excel die Steuerung an die XLL übergeben hat. Eine Tabellenfunktion, die von Excel aufgerufen wird, kann Excel mithilfe der C-API zurückrufen. Ein XLL-Befehl, der von Excel aufgerufen wird, kann die C-API aufrufen. DLL- und XLL-Funktionen und Befehle, die von VBA aufgerufen, wenn VBA wiederum selbst von Excel aufgerufen wurde, können die C-API aufrufen. Sie können beispielsweise keinen zeitlich festgelegten Windows-Rückruf in XLL festlegen und die C-API von dort aufrufen, und Sie können die C-API nicht von einem Hintergrundthread aufrufen, der von XLL erstellt wurde. Das asynchrone Aufrufen von Excel mithilfe von Com von einer DLL- oder XLL-Funktion aus wird nicht empfohlen.
  
Dies ist sehr einschränkend, denn es gibt möglicherweise Anwendungen, in denen Sie möchten, dass Excel auf ein Ereignis asnychron reagiert. Vielleicht möchten Sie beispielsweise, dass Excel ein Datenstück im Internet abruft und erneut berechnet, wenn sich die Daten ändern. Oder Sie möchten, dass ein Hintergrundthread eine Berechnung ausführt und Excel diese nach Abschluss neu berechnet.
  
Sie erreichen dies, indem Sie Excel aktiv Änderungen abfragen lassen, dies ist ineffizient ist und einschränkend, da Excel dabei häufig seine normale Aktivität unterbrechen muss. Sie können zwar mithilfe der C-API oder VBA einen wiederholten zeitgesteuerten Befehl einrichten, dies ist aber keine ideale Lösung.
  
Im Idealfall benötigen Sie einen effizienteren externen Prozess, der nach der Änderung von Daten sucht, und dieser externe Prozess soll auslösen, dass Excel das Update abruft und eine Neuberechnung durchführt. Hierfür können Sie eine Anwendung verwenden, die über COM eine Schnittstelle mit Excel bildet. COM ist nicht wie die C-API darauf beschränkt, nur dann Aufrufen zu tätigen, wenn Excel seine Steuerung ausdrücklich übergeben hat. COM-Anwendungen können Excel-Methoden aufrufen, wenn Excel den Status "Bereit" aufweist, diese Methodenaufrufe werden jedoch möglicherweise ignoriert, wenn Dialogfelder angezeigt werden, Menüs abgerufen werden oder wenn ein Makro ausgeführt wird.
  
## <a name="c-api-and-its-relation-to-xlm"></a>Die C-API und ihre Beziehung zu XLM

Die Excel-Makrosprache (XLM) war die erste Programmierumgebung in Excel, auf die der Benutzer zugreifen konnte. Mit dieser Sprache konnten Benutzer benutzerdefinierte Befehle und Funktionen in speziellen Makrovorlagen erstellen, die wie normale Arbeitsblätter aussehen. XLM-Makrovorlagen werden in Excel 2013 immer noch unterstützt. Zusätzlich zu den folgenden Elementen, die in einem Arbeitsblatt nicht eingegeben werden können, könnenSie alle gewöhnlichen Tabellenblattfunktion wie **SUM** und **LOG** in einer Makrovorlage verwenden: 
  
- Funktionen für Arbeitsbereichsinformationen wie **GET.CELL** und **GET.WORKBOOK**.
    
- Funktionen, die Befehlen entsprechen, die eine Automatisierung gewöhnlicher Benutzervorgänge ermöglichen, z. B. **DEFINE.NAME** und **PASTE**.
    
- Funktionen, die im Zusammenhang mit Add-Ins stehen, z. B. **REGISTER**.
    
- Ereignistraps, die Befehlen entsprechen, z. B. **ON.ENRTY** und **ON.TIME**.
    
- Makrofunktionsspezifische Operationen wie **ARGUMENT** und **VOLATILE**.
    
- Flusssteuerungsoperationen wie **GOTO** und **RETURN**.
    
In Excel, Version 3, gab es eine einschränkte Version der C-API. In Excel, Version 4, wurde die XLM-Sprache jedoch der C-API zugeordnet. Seitdem können DLLs alle Tabellenblattfunktionen, Funktionen für Makrovorlageninformationen und Befehle aufrufen und Ereignistraps festlegen. DLLs können aus der C-API heraus keine XLM-Flusssteuerungsfunktionen aufrufen. Diese Makrovorlagenfunktionen und Befehle sind in der Hilfedatei "XLMacr8.hlp" (bisher bezeichnet als "Macrofun.hlp") dokumentiert. Um diese Hilfedatei abzurufen, rufen Sie das [Microsoft Download Center](http://download.microsoft.com) auf, und suchen Sie nach "XLMacr8.hlp". 
  
> [!NOTE]
> In Windows Vista und Windows 7 werden HLP-Dateien nicht direkt unterstützt, Sie können aber das [Windows-Hilfeprogramm (WinHlp32.exe) für Windows Vista](http://go.microsoft.com/fwlink/?LinkID=82148) oder das [Windows-Hilfeprogramm (WinHlp32.exe) für Windows 7](http://www.microsoft.com/download/en/details.aspx?id=91) von Microsoft herunterladen und die Dateien damit öffnen. 
  
DLLs rufen C-API-Entsprechungen dieser Funktionen und Befehle mithilfe der Rückruffunktionen **Excel4**, **Excel4v**, **Excel12** und **Excel12v** auf (die beiden letzten wurden in Excel 2007 eingeführt). Aufgezählte Konstanten, die den einzelnen Funktionen und Befehlen entsprechen, sind in einer Headerdatei definiert und werdenals eines der Argumente an diese Rückrufe übergeben. **GET.CELL** wird beispielsweise durch **xlfGetCell**, **REGISTER** durch **xlfRegister** und **DEFINE.NAME** durch **xlcDefineName** dargestellt.
  
Abgesehen davon, dass die Tabellenblattfunktionen und Makrovorlagenfunktionen und Befehle bereitgestellt werden, liefert die C-API Funktions- und Befehlsaufzählungen, die nur mithilfe dieser Rückrufe innerhalb einer DLL aufgerufen werden können. Mit **xlGetName** kann eine DLL beispielsweise ihren eigenen vollständigen Pfad und Dateinamen ermitteln, der für die Registrierung von Funktionen und Befehlen bei Excel erforderlich ist. 
  
Seit der Einführung von VBA-Blättern (Visual Basic for Applications) in Excel, Version 5, und des Visual Basic-Editors (VBE) in Version 8 (Excel 97), besteht die einfachste Möglichkeit für Benutzer zum Anpassen von Excel darin, VBA anstele von XLM zu verwenden. Daher ist ein Großteil der neuen Funktionalität, die in späteren Verseionen von Excel eingeführt wurde, über VBA, jedoch nicht über XLM oder die C-API verfügbar.
  
Weitere Informationen finden Sie unter [Was ist neu in der C-API für Excel 2013](what-s-new-in-the-c-api-for-excel.md).
  
## <a name="see-also"></a>Siehe auch



[Was ist neu in der C-API für Excel](what-s-new-in-the-c-api-for-excel.md)
  
[C-API-Rückruffunktionen Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)


[Erste Schritte mit dem Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

