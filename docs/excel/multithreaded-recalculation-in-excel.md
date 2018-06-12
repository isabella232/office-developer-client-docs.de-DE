---
title: Multithreaded neuberechnung in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- thread-safe cells [excel 2007],multithreading in Excel,concurrent tasks [Excel 2007],thread-safe functions [Excel 2007],multithreaded recalculation [Excel 2007],MTR [Excel 2007],XLL functions [Excel 2007], registering as thread safe,recalculation [Excel 2007], multithreaded,memory contention [Excel 2007],registering XLL functions as thread safe [Excel 2007],unsafe functions [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790556"
---
# <a name="multithreaded-recalculation-in-excel"></a>Multithreaded neuberechnung in Excel

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Office Excel 2007 war die erste Version von Excel, in der die Multithread-Neuberechnung (MTR) f�r Arbeitsbl�tter verwendet wurde. Sie k�nnen Excel f�r die Verwendung von bis zu 1.024 gleichzeitigen Threads bei der Neuberechnung konfigurieren, unabh�ngig von der Anzahl von Prozessoren oder Prozessorkernen auf dem Computer. 
  
> [!NOTE]
> [!HINWEIS] Da mit jedem Thread ein Betriebssystemmehraufwand verbunden ist, sollten Sie Excel nicht f�r die Verwendung von mehr Threads als erforderlich konfigurieren. 
  
Wenn der Computer �ber mehrere Prozessoren oder Prozessorkerne verf�gt, �bernimmt das Betriebssystem die Verantwortung f�r die effizienteste Zuweisung von Threads zu den Prozessoren.
  
## <a name="excel-mtr-overview"></a>Übersicht über die Excel MTR

Excel versucht, die Teile der Berechnungskette zu identifizieren, die in verschiedenen Threads gleichzeitig neu berechnet werden k�nnen. Die folgende sehr einfache Struktur (bei der x ? y bedeutet, dass y nur von x abh�ngt) zeigt ein Beispiel daf�r.
  
**Abbildung 1: Gleichzeitiges Berechnen in verschiedenen Threads**

![Berechnung der gleichzeitig auf verschiedenen threads] (media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Berechnung der gleichzeitig auf verschiedenen threads")
  
Nachdem A1 berechnet ist, k�nnen A2 und dann A3 in einem Thread berechnet werden, w�hrend B1 und dann C1 in einem anderen Thread berechnet werden, vorausgesetzt, dass alle Zellen threadsicher sind. 
  
> [!NOTE]
> [!HINWEIS] Der Begriff threadsichere Zelle bedeutet, dass eine Zelle nur threadsichere Funktionen enth�lt. Was und was nicht threadsicher ist, wird ausf�hrlich [Was von Excel als threadsicher betrachtet wird und was nicht](#xl2007xllsdk_threadsafe) erl�utert. 
  
Die meisten praktischen Arbeitsmappen enthalten viel komplexere Abh�ngigkeitsstrukturen als dieses Beispiel. Dar�ber hinaus ist die Neuberechnungszeit einer Zelle erst bekannt, wenn eine Berechnung abgeschlossen ist und kann je nach Argumenten der Funktion stark variieren. F�r optimale Ergebnisse versucht Excel, die Berechnungsreihenfolge f�r jede Berechnung zu optimieren, bis keine weitere Optimierung m�glich ist.
  
Excel verwendet einen einzelnen Hauptthread, um Folgendes auszuf�hren:
  
- Integrierte Befehle
    
- XLL-Befehle
    
- XLL-Add-in-Manager-Schnittstellenfunktionen (**XlAutoOpen** Funktion usw.) 
    
- Benutzerdefinierte Befehle von Microsoft Visual Basic for Applications (VBA) (oft als Makros bezeichnet)
    
- Benutzerdefinierte VBA-Funktionen
    
- Integrierte threadunsichere Arbeitsblattfunktionen (eine Liste finden Sie im n�chstem Abschnitt)
    
- Benutzerdefinierte XLM-Makroarbeitsblattbefehle und -funktionen
    
- COM-Add-In-Befehle und -Funktionen
    
- Funktionen und Operatoren in Ausdr�cken f�r bedingte Formatierung
    
- Funktionen und Operatoren in definierten Namensdefinitionen, die in Arbeitsblattformeln verwendet werden
    
- Die erzwungene Auswertung eines Ausdrucks im Feld f�r die Formelbearbeitung mithilfe der **F9** -TASTE 
    
Alle Arbeitsblattformeln, unabh�ngig davon, ob die Funktionen threadsicher sind oder nicht, werden im Hauptthread ausgewertet, es sei denn, Excel ist f�r die Verwendung von mehr als einem Thread konfiguriert. Wenn der Benutzer angibt, dass mehrere Threads verwendet werden sollen, werden die zus�tzlichen Threads f�r threadsichere Zellen verwendet. Beachten Sie, dass der Hauptthread m�glicherweise weiterhin f�r threadsichere Zellen verwendet wird, wenn dies aus Sicht des Lastenausgleichs sinnvoll ist.
  
Es lohnt sich, erneut zu erw�hnen, dass Excel nicht mehr als einen Befehl gleichzeitig ausf�hrt, daher m�ssen Sie nicht dieselben Vorsichtsma�nahmen wie beim Schreiben von threadsicheren Funktionen anwenden, z. B. die Verwendung von threadlokalem Speicher und kritischen Bereichen.
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a>Was ist und nicht als Thread sicherer von Excel
<a name="xl2007xllsdk_threadsafe"> </a>

Excel betrachtet nur Folgendes als threadsicher:
  
- Alle un�ren und bin�ren Operatoren in Excel
    
- Nahezu alle integrierten Arbeitsblattfunktionen beginnend in Excel 2007 (siehe Ausnahmenliste)
    
- XLL-Add-In-Funktionen, die ausdr�cklich als threadsicher registriert wurden
    
Die folgenden integrierten Arbeitsblattfunktionen sind nicht threadsicher:
  
- **PHONETIC**
    
- **CELL**, wenn das Argument �format" oder �address" verwendet wird 
    
- **INDIRECT**
    
- **GETPIVOTDATA**
    
- **CUBEMEMBER**
    
- **CUBEVALUE**
    
- **CUBEMEMBERPROPERTY**
    
- **CUBESET**
    
- **CUBERANKEDMEMBER**
    
- **CUBEKPIMEMBER**
    
- **CUBESETCOUNT**
    
- **ADDRESS**, wenn der f�nfte Parameter (sheet_name) vorgegeben ist 
    
- Jede Datenbankfunktion (**DSUM**, **DAVERAGE**usw.), die auf eine Pivot-Tabelle verweist
    
- **FEHLER. TYP**
    
- **HYPERLINK**
    
Die folgenden Funktionen werden ausdr�cklich als unsicher betrachtet:
  
- Benutzerdefinierte VBA-Funktionen
    
- Benutzerdefinierte COM-Add-In-Funktionen
    
- Benutzerdefinierte XLM-Makroarbeitsblattfunktionen
    
- XLL-Add-In-Funktionen, die nicht ausdr�cklich als threadsicher registriert sind
    
Die Auswirkung ist, dass die folgenden Vorg�nge und Funktionen nicht threadsicher sind und ein Fehler auftritt, wenn sie von einer XLL-Funktion aufgerufen werden, die als threadsicher registriert ist:
  
- Anrufe an Informationen XLM-Funktionen, beispielsweise **XlfGetCell** (**GET. Zelle**).
    
- Anrufe an **XlfSetName** (**SET.NAME**) und Löschen von XLL-interne Namen definieren.
    
- Aufrufe an threadunsichere benutzerdefinierte Funktionen �ber **xlUDF**
    
- Aufrufe an die Funktion [xlfEvaluate](xlfevaluate.md) f�r Ausdr�cke, die threadunsichere Funktionen oder definierte Namen enthalten, deren Definitionen threadunsichere Funktionen enthalten 
    
- Aufrufe an die Funktion [xlAbort](xlabort.md) zum L�schen einer Unterbrechungsbedingung 
    
- Aufrufe an die Funktion [xlCoerce](xlcoerce.md) zum Abrufen des Werts eines nicht berechneten Zellenbezugs 
    
> [!NOTE]
> [!HINWEIS] XLL-Arbeitsblattfunktionen d�rfen keine C-API-Befehle wie **xlcSave** aufrufen, unabh�ngig davon, ob diese als threadsicher registriert wurden oder nicht. 
  
Angesichts der Tatsache, dass XLL-Funktionen, die als threadsicher deklariert sind, weder XLM-Informationsfunktionen aufrufen noch auf nicht berechnete Zellen verweisen k�nnen, l�sst Excel nicht zu, dass XLL-Funktionen, die als Makroarbeitsblattentsprechungen registriert sind, auch als threadsicher registriert werden k�nnen. Daher f�hrt der Versuch, den Wert eines nicht berechneten Zellenbezugs mithilfe von **xlCoerce** zu einem **xlretUncalced**-Fehler. Das Aufrufen einer XLM-Informationsfunktion f�hrt zu einem **xlretFailed**-Fehler. Die anderen zuvor aufgef�hrten Funktionen f�hren zu einem in der Excel-C-API eingef�hrten Fehlercode: **xlretNotThreadSafe**. 
  
Die reinen C-API-R�ckruffunktionen sind alle threadsicher:
  
- **xlCoerce** (au�er wenn dennoch ein Fehler bei der Koersion nicht berechneter Zellenbez�ge auftritt) 
    
- **xlFree**
    
- **xlStack**
    
- **xlSheetId**
    
- **xlSheetNm**
    
- **xlAbort** (au�er bei Verwendung zum L�schen einer Unterbrechungsbedingung) 
    
- **xlGetInst**
    
- **xlGetHwnd**
    
- **xlGetBinaryName**
    
- **xlDefineBinaryName**
    
Die einzige Ausnahme ist die Funktion **xlSet**, die in jedem Fall eine Befehlsentsprechung ist und daher von keiner Arbeitsblattfunktion aufgerufen werden kann. 
  
Eine XLL-Arbeitsblattfunktion kann bei Excel als threadsicher registriert werden. Dadurch wird Excel angewiesen, dass die Funktion sicher und gleichzeitig in mehreren Threads aufgerufen werden kann, Sie m�ssen jedoch sicherstellen, dass dies wirklich der Fall ist. Excel wird m�glicherweise destabilisiert, wenn eine als threadsicher registrierte Funktion sich dann unsicher verh�lt.
  
## <a name="registering-xll-functions-as-thread-safe"></a>Registrieren von XLL-Funktionen als threadsicheren
<a name="xl2007xllsdk_threadsafe"> </a>

Folgende Regeln muss ein Entwickler beim Schreiben threadsicherer Funktionen beachten:
  
- Rufen Sie Ressourcen nicht in anderen DLLs auf, die m�glicherweise nicht threadsicher sind.
    
- F�hren Sie keine threadunsicheren Aufrufe �ber die C-API oder COM durch.
    
- Sch�tzen Sie Ressourcen, die gleichzeitig von mehreren Threads werden k�nnen, mithilfe von kritischen Bereichen.
    
- Verwenden Sie threadlokalen Speicher als threadspezifischen Speicher, und ersetzen Sie statische Variablen in Funktionen durch threadlokale Variablen.
    
Excel legt eine weitere Einschr�nkung auf: Threadsichere Funktionen k�nnen nicht als Makrovorlagenentsprechungen registriert werden und deshalb weder XLM-Informationsfunktionen aufrufen noch die Werte nicht neu berechneter Zellen abrufen.
  
## <a name="memory-contention"></a>Arbeitsspeicher Konflikte
<a name="xl2007xllsdk_threadsafe"> </a>

Multithread-Systeme m�ssen zwei wichtige Probleme ber�cksichtigen:
  
- Wie Speicher gesch�tzt werden kann, aus dem von mehr als einem Thread gelesen bzw. an den von mehr als einem Thread geschrieben wird
    
- Wie die Erstellung von und der Zugriff auf Speicher erfolgen soll, der dem ausf�hrenden Thread zugeordnet und deshalb f�r diesen privat ist
    
Das Windows-Betriebssystem und das Windows Software Development Kit (SDK) bieten Tools f�r beide F�lle: kritische Bereiche und die threadlokale Speicher-API (TLS-API). Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
Das erste Problem kann beispielsweise auftreten, wenn zwei Tabellenfunktionen (oder zwei gleichzeitig ausgef�hrte Instanzen derselben Funktion) auf eine globale Variable in einem DLL-Projekt zugreifen oder diese �ndern m�ssen. Denken Sie daran, dass eine solche globale Variable m�glicherweise in einer global zug�nglichen Instanz eines Klassenobjekts verborgen ist.
  
Das zweite Problem kann z. B. auftreten, wenn eine Tabellenfunktion eine statische Variable oder ein Objekt innerhalb des Funktionsrumpfcodes deklariert. Der C/C++-Compiler erstellt nur eine einzelne Kopie, die von allen Threads verwendet wird. Das bedeutet, dass eine Instanz der Funktion den Wert �ndern k�nnte, w�hrend eine andere in einem anderen Thread m�glicherweise davon ausgeht, dass der Wert dem entspricht, was sie zuvor festgelegt hat.
  
## <a name="example-applications-of-mtr"></a>Beispiel-Clientanwendungen von MTR
<a name="xl2007xllsdk_threadsafe"> </a>

Alle XXLs, die Tabellenfunktionen exportieren, k�nnen die Multithread-Neuberechnung (MTR) in Excel nutzen, vorausgesetzt, dass diese Funktionen keine threadunsicheren Aktionen durchf�hren m�ssen. Damit kann Excel Arbeitsmappen, die von diesen abh�ngen, so schnell wie m�glich neu berechnen, was unabh�ngig von der Anwendung w�nschenswert ist.
  
MTR hat insbesondere eine enorme Auswirkung auf die Neuberechnungszeit f�r Arbeitsmappen, die benutzerdefinierte Funktionen (User-Defined Functions, UDFs) aufrufen, die wiederum selbst externe Prozesse aufrufen, um das gew�nschte Ergebnis abzurufen. Denken Sie insbesondere an eine UDF, die einen Remoteserver aufruft, der viele Anforderungen gleichzeitig verarbeiten kann, und eine Arbeitsmappe, die viele Aufrufe an diese Funktion enth�lt. Wenn eine Singlethread-Neuberechnung der Arbeitsmappe erfolgt, muss jeder Aufruf an die UDF, und damit an den Remoteserver, abgeschlossen werden, bevor der n�chste erfolgen kann. Damit wird die F�higkeit des Servers aufgehoben, viele Aufrufe auf einmal zu verarbeiten. Bei einer Multithread-Neuberechnung der Arbeitsmappe kann Excel mehrere Aufrufe gleichzeitig oder in schneller Folge durchf�hren.
  
Wenn Excel f�r die Verwendung derselben Anzahl von Threads wie der Server konfiguriert ist � nennen wir es N � und die Topologie der Abh�ngigkeitsstruktur der Arbeitsmappe es zul�sst, k�nnte die gesamte Neuberechnungszeit auf nahezu 1/N der Singlethread-Berechnungszeit verringert werden. Das trifft m�glicherweise sogar zu, wenn der Clientcomputer (auf dem die Arbeitsmappe ausgef�hrt wird) nur einen Prozessor enth�lt, insbesondere, wenn die Zeit f�r den Aufruf an den Server relativ kurz im Vergleich zu der Zeit ist, den Server zum Verarbeiten des Aufrufs ben�tigt. 
  
F�r jeden zus�tzlichen Thread gibt es einen Betriebssystemmehraufwand. Damit ist f�r eine bestimmte Arbeitsmappe sowie einen bestimmten Server und Clientcomputer m�glicherweise ein gewisses Experimentieren erforderlich, um die optimale Anzahl von Threads zu finden, die Excel verwenden sollte. 
  
Betrachten Sie beispielsweise einen Computer mit einem einzigen Prozessor, auf dem Excel und eine Arbeitsmappe mit 1.000 Zellen ausgef�hrt werden. Es erfolgt ein Aufruf an eine UDF, die wiederum einen oder mehrere Remoteserver aufruft. Nehmen wir an, dass die 1.000 Zellen nicht voneinander abh�ngig sind, sodass Excel nicht darauf warten muss, dass ein Aufruf abgeschlossen ist, bevor der n�chste Aufruf erfolgen kann. (Eine gewisse Lockierung dieser Einschr�nkung ist ohne Auswirkung auf das Beispiel m�glich.) Wenn die Server 100 Anforderungen gleichzeitig verarbeiten k�nnen und Excel f�r die Verwendung von 100 Threads konfiguriert ist, kann die Ausf�hrungszeit auf nur 1/100 der Zeit reduziert werden, wenn nur ein einziger Thread verwendet wird. Die Mehraufwand, der damit verbunden ist, dass Excel Aufrufe zu jedem Thread zuordnet, und die Tatsache, dass das Betriebssystem 100 Threads verwaltet, bedeuten, dass die Reduzierung in der Praxis nicht ganz so gro� ausf�llt. Hier wird au�erdem ausdr�cklick angenommen, dass der Server gut skaliert ist und sich die Aufforderung, 100 Aufgaben gleichzeitig zu verarbeiten, nicht signifikant auf die Abschlusszeiten einzelner Aufgaben auswirkt.
  
Eine praktische Anwendung, in der dieses Verfahren einen wichtigen Vorteil haben kann, sind die Monte-Carlo-Methode und andere zahlenintensive Aufgaben, die in kleinere Unteraufgaben aufgeteilt werden k�nnen, die an Server vergeben werden k�nnen.
  
## <a name="excel-services-considerations"></a>Excel Services-Überlegungen
<a name="xl2007xllsdk_threadsafe"> </a>

Excel Services unterst�tzt das Laden, Berechnen und Rendern von Excel-Tabellen auf einem Server. Benutzer k�nnen dann �ber Standardbrowsertools auf die Tabellen zugreifen und mit diesen interagieren.
  
Excel Services-UDFs werden mithilfe von verwaltetem Microsoft .NET Framework-Code erstellt und �ber eine .NET-Assembly zur Verf�gung gestellt. XLLs werden von Excel Services nicht unterst�tzt. Eine Server-UDF-Ressource mit verwaltetem Code kann eine XLL aufrufen, um auf ihre Funktionalit�t zuzugreifen, sodass der Benutzer mit einer auf dem Server geladenen Arbeitsmappe dieselben Funktionen hat wie mit einer auf dem Client geladenen Arbeitsmappe.
  
Um die Funktionen einer XLL auf diese Weise verf�gbar zu machen, m�ssen sie von einer .NET-Assembly umschlossen werden, die Argumente und R�ckgabewerte von den systemeigenen Datentypen in die verwalteten .NET Framework-Datentypen konvertiert und die XLL-Funktionen aufruft. Der .NET-Wrapper w�rde jeweils eine Server-UDF f�r jede XLL-Funktion exportieren, auf die zugegriffen wird. Eine weitere Voraussetzung ist, dass XLL-Funktionen, die auf diese Weise aufgerufen werden, threadsicher sein m�ssen. Da die XLL-Funktionen nicht auf dieselbe der Weise wie beim Excel-Client registriert sind, k�nnen der Server und der .NET-Wrapper nicht erzwingen, dass sie threadsicher sind. Es liegt in der Verantwortung des XLL-Entwicklers, dies sicherzustellen.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Neuberechnung](excel-recalculation.md)  
- [Speicherverwaltung in Excel](memory-management-in-excel.md) 
- [Zugriff auf XLL-Code in Excel (engl.)](accessing-xll-code-in-excel.md)  
- [Excel-Programmierkonzepte](excel-programming-concepts.md)  
- [Excel XLL-SDK-API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

