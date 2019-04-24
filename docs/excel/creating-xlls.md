---
title: Erstellen von XLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- DLLs [Excel 2007], Aufrufen in Excel,xlAutoFree-Funktion [Excel 2007],xlAutoFree12-Funktion [Excel 2007],xlcall32.lib [Excel 2007],xlAutoRegister-Funktion [Excel 2007],xlcall.cpp [Excel 2007],xlAutoRemove-Funktion [Excel 2007],xlAddInManagerInfo-Funktion [Excel 2007],xlAutoAdd-Funktion [Excel 2007],xlAutoOpen-Funktion [Excel 2007],xlAutoClose-Funktion [Excel 2007],DLLs [Excel 2007], Umwandeln in XLLs,XLLs [Excel 2007], Aufrufen in Excel,xlAutoRegister12-Funktion [Excel 2007],xlcall.h [Excel 2007],xlAddInManagerInfo12-Funktion [Excel 2007]
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 886b8e74f00f2e724785d43475ee0ffa3c922710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304144"
---
# <a name="creating-xlls"></a>Erstellen von XLLs

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wenn Ihre DLL eigenständig ist oder sich nur auf andere Bibliotheken stützt, müssen Sie wissen, wie Sie Microsoft Excel aktivieren, um Zugriff auf die zugehörigen Funktionen und Befehle zu erhalten. Weitere Informationen finden Sie unter [Zugreifen auf DLLs in Excel](how-to-access-dlls-in-excel.md). 
  
Wenn Ihre DLL jedoch auf die Excel-Funktionalität zugreifen muss (z. B. um den Inhalt einer Zelle abzurufen, eine Arbeitsblattfunktion aufzurufen oder Excel nach Informationen zum Arbeitsbereich abzufragen), muss Ihr Code einen Rückruf in Excel vornehmen können.
  
Die C-API von Excel bietet mehrere Funktionen, mit denen DLLs einen Rückruf in Excel vornehmen können. Damit die DLL auf diese Funktionen zugreifen kann, muss sie zur Kompilierzeit statisch mit der 32-Bit-Bibliothek von Excel (xlcall32.lib) verknüpft werden. Die statische Bibliothek kann von Microsoft als Teil des Microsoft Excel 2013 XLL SDKs heruntergeladen werden, das sowohl die 32-Bit- als auch die 64-Bit-Version dieser Bibliothek enthält.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Aktivieren von DLLs für den Rückruf in Excel

Damit eine DLL auf die Funktionen in Excel zugreifen und Arbeitsbereichsinformationen abrufen oder festlegen kann, muss sie zunächst die Adressen der Excel-Rückruffunktionen **Excel4**, **Excel4v**, **Excel12** und **Excel12v** abrufen. Die beiden letzten Funktionen wurden in Excel 2007 eingeführt und sind in nachfolgenden Versionen verfügbar. Um auf all diese Funktionen zuzugreifen, muss das DLL-Projekt Verweise auf die folgenden Dateien aus dem Excel 2013 XLL SDK enthalten. Wenn Sie nur auf die beiden ersten Rückruffunktionen (in jeder Excel-Version enthalten) zugreifen möchten, muss Ihr Projekt nur die beiden ersten Dateien enthalten.
  
### <a name="xlcallh"></a>Xlcall.h

Die Datei "Xlcall.h" enthält die folgenden Elemente:
  
- Funktionsprototypen für alle Rückruffunktionen.
    
- Definitionen der Datenstrukturen, welche die Rückruffunktionen für den Austausch von Daten zwischen DLL/XLL und Excel verwenden, und Definitionen von Datentypkonstanten.
    
- Definitionen der C-API-Funktion und Befehlsentsprechungen für Arbeitsblatt, Makroblattfunktionen und unterstützte Excel-Befehle.
    
- Definitionen der Rückgabewerte der Rückruffunktion.
    
Sie sollten für diese Datei die Direktive **#include** (direkt oder indirekt über eine andere Headerdatei) in allen Dateien verwenden, die auf die C-API zugreifen oder die Datentypen verarbeiten, die von der C-API verwendet werden. 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

Die Bibliothek "Xlcall32.lib" exportiert die beiden ersten Rückruffunktionen **Excel4** und **Excel4v** sowie die **XlCallVer**-Funktion. Ohne einen Verweis auf diese Bibliothek in Ihrem Projekt kann der Linker die XLL nicht erstellen, wenn Sie einen dieser Rückrufe in Ihrem Code verwendet haben. (Die Adressen dieser Funktionen können Sie durch eine dynamische Verknüpfung mit der entsprechenden Xlcall32.dll beziehen, die im Rahmen einer normalen Excel-Installation auf Ihr System kopiert wird.) 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Die Excel-Rückruffunktionen **Excel12** und **Excel12v** werden nicht in Xlcall32.lib exportiert. Dadurch wird sichergestellt, dass XLL-Projekte, die Sie ab Excel 2007 erstellen, auch mit früheren Excel-Versionen funktionieren. Das Modul "Xlcall.cpp" enthält Code für die Funktionen **Excel12** und **Excel12v**, die ab Excel 2007 einen Excel-Einstiegspunkt aufrufen oder den Wert "safe error" (sicherer Fehler) zurückgeben, wenn Sie eine frühere Version von Excel ausführen. Sie sollten dieses Modul in Ihr Projekt einbeziehen, wenn Sie eine XLL erstellen möchten, die in Excel 2007 oder höher ausgeführt werden und in der Lage sein soll, die neuen Datentypen zu verwenden, die größere Raster und längere Unicode-Zeichenfolgen verarbeiten können. 
  
> [!NOTE]
> Ab dem Excel 2010 SDK kann diese Datei sowohl für 32-Bit- als auch 64-Bit-XLLs kompiliert werden. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>Umwandeln von DLLs in XLLs: Add-In-Manager und Schnittstellenfunktionen

Eine XLL ist eine DLL, die mehrere Prozeduren exportiert, die von Excel oder dem Add-In-Manager von Excel aufgerufen werden. Diese Prozeduren sind hier kurz beschrieben und werden ausführlich unter [Add-In-Manager und XLL-Schnittstellenfunktionen](add-in-manager-and-xll-interface-functions.md) behandelt. All diese DLL-Rückrufe beginnen mit dem Präfix **xlAuto**. Nur einer der Rückrufe, der Befehl **xlAutoOpen**, ist erforderlich. Er wird beim Aktivieren des Add-Ins aufgerufen und wird in der Regel zum Registrieren von XLL-Funktionen und -Befehlen mit Excel und für andere Initialisierungsaufgaben verwendet. Die Funktionssignaturen und Beispielimplementierungen aller **xlAuto**-Funktionen finden Sie in den nachfolgenden Abschnitten. 
  
Obwohl nur **xlAutoOpen** als Rückruffunktion erforderlich ist, muss das Add-In möglicherweise auch andere Funktionen exportieren. Das hängt vom Verhalten des Add-Ins ab. 
  
In Excel 2007 wurde der neue Datentyp **XLOPER12** eingeführt, um größere Raster und lange Unicode-Zeichenfolgen zu unterstützen. **XLOPER12** wird weiter unten in diesem Thema beschrieben. Während **xlAuto**-Funktionen den alten Datentyp **XLOPER** übernehmen oder zurückgeben, wurden in Excel 2007 neue Versionen dieser Funktionen eingeführt, welche die Datentypen **XLOPER12** verwenden. Mit Ausnahme der **xlAutoFree12**-Funktion, die Sie manchmal zur Vermeidung von **XLOPER12**-Speicherverlusten implementieren müssen, können Sie bedenkenlos auf alle **xlAuto**-Funktionen der Version 12 verzichten. In diesem Fall ruft Excel (ab Excel 2007) die **XLOPER**-Versionen auf. 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel ruft jedes Mal, wenn die XLL aktiviert wird, die [xlAutoOpen](xlautoopen.md)-Funktion auf. Das Add-In wird zu Beginn einer Excel-Sitzung aktiviert, wenn es in der letzten Excel-Sitzung, die ordnungsgemäß beendet wurde, aktiv war. Das Add-In wird aktiviert, wenn es während einer Excel-Sitzung geladen werden. Das Add-In kann während einer Excel-Sitzung deaktiviert und erneut aktiviert werden. Bei der erneuten Aktivierung wird die Funktion aufgerufen. 
  
Verwenden Sie **xlAutoOpen**, um XLL-Funktionen und -Befehle zu registrieren, Datenstrukturen zu initialisieren, die Benutzeroberfläche anzupassen usw. 
  
Wenn das Add-In die [xlAutoRegister](xlautoregister-xlautoregister12.md)-Funktion oder die [xlAutoRegister12](xlautoregister-xlautoregister12.md)-Funktion implementiert und exportiert, versucht Excel möglicherweise, eine Funktion oder einen Befehl zu aktivieren und zu registrieren, ohne zuerst die **xlAutoOpen**-Funktion aufzurufen. In diesem Fall müssen Sie sicherstellen, dass das Add-In für die Funktion oder den Befehl ausreichend initialisiert ist, damit es ordnungsgemäß funktioniert. Wenn das nicht zutrifft, sollten Sie entweder den Versuch, die Funktion oder den Befehl zu registrieren, abbrechen oder die erforderliche Initialisierung ausführen. 
  
### <a name="xlautoclose"></a>xlAutoClose

Excel ruft jedes Mal, wenn die XLL deaktiviert wird, die [xlAutoClose](xlautoclose.md)-Funktion auf. Das Add-in wird deaktiviert, wenn eine Excel-Sitzung ordnungsgemäß beendet wird. Wenn der Benutzer während einer Excel-Sitzung das Add-In deaktiviert, wird die Funktion aufgerufen. 
  
Verwenden Sie **xlAutoClose**, um die Registrierung von Funktionen und Befehlen aufzuheben, Ressourcen freizugeben, Anpassungen rückgängig zu machen usw. 
  
> [!NOTE]
> Bei der Aufhebung der Registrierung von Funktionen und Befehlen gibt es ein bekanntes Problem. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel ruft jedes Mal, wenn der Benutzer während einer Excel-Sitzung die XLL mithilfe des Add-In-Managers aktiviert, die [xlAutoAdd](xlautoadd.md)-Funktion auf. Diese Funktion wird nicht aufgerufen, wenn Excel startet und ein vorinstalliertes Add-In lädt. 
  
Sie können diese Funktion verwenden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer mitteilt, dass das Add-In zum Lesen oder Schreiben in der Registrierung oder zum Überprüfen von Lizenzinformationen aktiviert wurde.
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel ruft jedes Mal, wenn der Benutzer während einer Excel-Sitzung die XLL mithilfe des Add-In-Managers deaktiviert, die [xlAutoRemove](xlautoremove.md)-Funktion auf. Diese Funktion wird nicht aufgerufen, wenn eine Excel-Sitzung mit dem installierten Add-In (ordnungsgemäß oder unerwartet) beendet wird. 
  
Sie können diese Funktion verwenden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer mitteilt, dass das Add-In zum Lesen oder Schreiben in der Registrierung deaktiviert wurde.
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

Excel ruft die [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md)-Funktion auf, wenn der Add-In-Manager zum ersten Mal in einer Excel-Sitzung aufgerufen wird. Wenn Excel ein Argument gleich 1 übergibt, sollte diese Funktion eine Zeichenfolge (in der Regel der Name des Add-Ins) zurückgeben. Andernfalls sollte **#VALUE!** zurückgegeben werden.
  
Ab Excel 2007 ruft Excel bevorzugt die **xlAddInManagerInfo12**-Funktion statt der **xlAddInManagerInfo**-Funktion auf, wenn sie von der XLL exportiert wird. Die **xlAddInManagerInfo12**-Funktion sollte auf die gleiche Weise funktionieren wie die **xlAddInManagerInfo**-Funktion, um versionsspezifische Unterschiede im Verhalten der XLL zu vermeiden. Die **xlAddInManagerInfo12**-Funktion sollte den Datentyp **XLOPER12** zurückgeben, während die **xlAddInManagerInfo**-Funktion den Datentyp **XLOPER ** zurückgeben sollte. 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

Excel ruft jedes Mal, wenn ein Aufruf der XLM-Funktion **REGISTER** oder der entsprechenden C-API-Funktion [xlfRegister](xlfregister-form-1.md) erfolgt, die [xlAutoRegister](xlautoregister-xlautoregister12.md)-Funktion auf, wobei der zu registrierenden Funktion Rückgabe- und Argumenttypen fehlen. Die **xlAutoRegister**-Funktion ermöglicht der XLL, die internen Listen mit exportierten Funktionen und Befehlen zu durchsuchen, um die Funktion mit dem Argument zu registrieren und die angegebenen Typen zurückzugeben. 
  
Ab Excel 2007 ruft Excel bevorzugt die **xlAddInRegister12**-Funktion statt der **xlAddInRegister**-Funktion auf, wenn sie von der XLL exportiert wird. 
  
> [!NOTE]
> Wenn **xlAddInRegister**/ **xlAddInRegister12** versucht, die Funktion zu registrieren, ohne Argument und Rückgabetypen bereitzustellen, tritt eine rekursive Aufrufschleife und in der Folge ein Aufruflistenüberlauf auf, der dazu führt, dass Excel beendet wird oder nicht mehr reagiert. 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel ruft die [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md)-Funktion auf, sobald eine XLL-Arbeitsblattfunktion den Datentyp **XLOPER**/ **XLOPER12** zurückgibt, und zwar mit einem Flag zur Information von Excel, dass Speicher vorhanden ist, den die XLL noch freigeben muss. Dadurch kann die XLL dynamisch zugewiesene Arrays, Zeichenfolgen und externe Verweise auf das Arbeitsblatt ohne Speicherverluste zurückgeben. Ab Excel 2007 wird der Datentyp **XLOPER12** unterstützt. Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
> [!NOTE]
> Ab Excel 2007 wird bei einer Konfiguration von Excel für die Verwendung der Multithread-Neuberechnung eines Arbeitsblatts die **xlAutoFree**/ **xlAutoFree12**-Funktion im selben Thread aufgerufen, der gerade zum Aufrufen der Funktion verwendet wurde, die ihn zurückgegeben hat. Der Aufruf von **xlAutoFree**/ **xlAutoFree12** erfolgt immer vor der Auswertung aller nachfolgenden Arbeitsblattzellen in diesem Thread. Dies vereinfacht das threadsichere Design in Ihrer XLL. Weitere Informationen finden Sie unter [Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Erstellen von 64-Bit-XLLs

Excel und benutzerdefinierte Funktionen können auf 64-Bit-Betriebssystemen ausgeführt werden, um die Leistungsvorteile gegenüber 32-Bit-Betriebssystemen zu nutzen. Excel übergibt Werte in **XLOPER12**-Strukturen, die Informationen zu den Typen für die Daten enthalten. Gehen Sie beim Konvertieren von Werten zwischen der **XLOPER12**-Struktur und nativen Typen wie **int** oder Zeigern mit Bedacht vor, um die Werte im größeren Typ beizubehalten. 
  
## <a name="see-also"></a>Weitere Artikel



[Aufrufen von XLL-Funktionen aus dem Funktionsassistenten oder Ersetzen von Dialogfeldern](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Add-In-Manager und XLL-Schnittstellenfunktionen](add-in-manager-and-xll-interface-functions.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

