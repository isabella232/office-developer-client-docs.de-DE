---
title: Erstellen von XLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- DLLs [excel 2007], Excel, XlAutoFree-Funktion [Excel 2007], xlAutoFree12-Funktion [Excel 2007],xlcall32.lib [Excel 2007], [Excel 2007],xlcall.cpp [Excel 2007], XlAutoRemove-Funktion [Excel 2007], XlAddInManagerInfo XlAutoRegister-Funktion aufruft Funktion [Excel 2007], XlAutoAdd-Funktion [Excel 2007], XlAutoOpen-Funktion [Excel 2007], XlAutoClose-Funktion [Excel 2007], DLLs [Excel 2007], Umwandeln in XLLs XLLs [Excel 2007], Excel, xlAutoRegister12-Funktion [Excel 2007],xlcall.h [Excel aufrufen 2007], xlAddInManagerInfo12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: de347d34768c25adf0d96642b4fade781ae26a9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790404"
---
# <a name="creating-xlls"></a>Erstellen von XLLs

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wenn die DLL eigenständig ist oder stützt sich nur auf andere Bibliotheken, müssen Sie zum Aktivieren von Microsoft Excel Zugriff auf seine Funktionen und Befehle kennen. Weitere Informationen finden Sie unter [Zugriff auf DLLs in Excel](how-to-access-dlls-in-excel.md). 
  
Jedoch, wenn die DLL muss Zugriff auf Excel-Funktionen (beispielsweise den Inhalt einer Zelle Aufrufen eine Tabellenfunktion oder Excel zum Abrufen von Informationen des Arbeitsbereichs abgefragt abrufen), muss der Code einen Rückruf in Excel können.
  
Der Excel-C-API bietet verschiedene Funktionen, mit denen DLLs in Excel zurückruft. Um auf diese zuzugreifen, die DLL verknüpft sein statisch zur Kompilierzeit mit der Excel-32-Bit-Bibliothek xlcall32.lib. Die statische Bibliothek ist zum Herunterladen von Microsoft als Teil der Microsoft Excel 2013 XLL-SDK, die 32-Bit- und 64-Bit-Versionen dieser Bibliothek enthält.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Aktivieren von DLLs Rückruf in Excel

Für eine DLL sein können den Zugriff auf die Funktionen in Excel und Abrufen oder festlegen Arbeitsbereichsinformationen, müssen sie zunächst die Adressen der Excel-Rückruffunktionen **Excel4**, **Excel4v**, **Excel12**und **Excel12v**abrufen. Die letzten beiden in Excel 2007 eingeführt wurden und in späteren Versionen verfügbar sind. Zugriff auf alle diese muss das DLL-Projekt Verweise auf die folgenden Dateien aus dem Excel 2013 XLL-SDK enthalten. Wenn Sie nur die ersten beiden Rückrufe (in einer Version von Excel) zugreifen möchten, muss das Projekt nur die ersten beiden Dateien enthalten.
  
### <a name="xlcallh"></a>Xlcall.h

Die Xlcall.h-Datei enthält die folgenden Elemente:
  
- Von Funktionsprototypen für alle Rückruffunktionen.
    
- Definitionen der Datenstrukturen, die die Rückrufe zum Austauschen von Daten zwischen der DLL/XLL und Excel verwenden und Datentyp Konstante.
    
- Definitionen von der C-API-Funktion und Befehl Entsprechungen des Arbeitsblatts, des Makro Blatt Funktionen und der unterstützten Excel-Befehle.
    
- Definitionen der Callback-Funktion geben Werte zurück.
    
Verwenden Sie die **#include** Richtlinie für diese Datei, die direkt oder indirekt über einen anderen Headerdatei in alle Dateien, die auf der C-API zugreifen oder behandelt Datentypen, die der C-API verwendet. 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

Die Xlcall32.lib Bibliothek exportiert die ersten beiden Rückrufe, **Excel4** und **Excel4v**und auch die **XlCallVer** -Funktion. Ohne einen Verweis auf diese Bibliothek in Ihrem Projekt kann nicht vom Linker XLL erstellt, wenn Sie eine der folgenden Rückrufe in Ihrem Code verwendet haben. (Sie erhalten die Adressen dieser Funktionen von dynamisch verknüpfen mit den entsprechenden Xlcall32.dll, die als Teil einer normalen Excel-Installation auf Ihr System kopiert werden.) 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Die Excel-Rückrufe **Excel12** und **Excel12v** werden nicht in Xlcall32.lib exportiert. Dadurch wird sichergestellt, dass XLL-Projekten, die Sie erstellen ab Excel 2007 mit früheren Versionen von Excel auch funktioniert. Das Modul Xlcall.cpp enthält Code für die **Excel12** und **Excel12v** -Funktionen, die in einem Excel-Eintrag aufrufen zeigen Sie in Excel 2007 starten oder einen sicheren Fehlerwert zurück, wenn Sie eine frühere Version von Excel ausgeführt werden. Sie sollten in diesem Modul in Ihrem Projekt einschließen, wenn Sie eine XLL, ausgeführt wird, starten in Excel 2007 und, ist die neue Datentypen verwenden, die größer Raster und länger Unicode-Zeichenfolgen behandeln, erstellen möchten. 
  
> [!NOTE]
> Beginnend mit Excel 2010 SDK, kann diese Datei für 32-Bit- und 64-Bit-XLLs kompiliert werden. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>Umwandeln von DLLs in XLLs: Add-In-Manager-Schnittstelle Funktionen

Eine XLL ist eine DLL, die verschiedene Prozeduren exportiert, die von Excel-Add-in-Manager oder Excel aufgerufen werden. Diese Verfahren sind hier kurz beschrieben und ausführlich im [Add-In - Manager und die Funktionen der XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md). Alle diese DLL Rückrufe beginnen mit dem Präfix **XlAuto**. Nur eine dieser Befehl **XlAutoOpen**, ist erforderlich. Es wird aufgerufen, wenn das Add-in ist aktiviert, und es wird gewöhnlich verwendet, Registrieren von XLL-Funktionen und Befehle mit Excel und für andere Aufgaben Initialisierung. In den nachfolgenden Abschnitten werden die Funktionssignaturen und Beispiel-Implementierung aller **XlAuto** -Funktionen bereitgestellt. 
  
Obwohl **XlAutoOpen** die einzige erforderliche diese Rückrufe ist, müssen Ihr Add-in auch andere Benutzer je nach dessen Verhalten zu exportieren. 
  
Excel 2007 eingeführt einen neuen Datentyp **XLOPER12**, für ein größerer Raster und zur Unterstützung von langer Unicode-Zeichenfolgen. **XLOPER12** wird weiter unten in diesem Thema beschrieben. Während die **XlAuto** -Funktionen nutzen oder zurückgeben den alten Datentyp **XLOPER**, wurden neue Versionen dieser Funktionen in Excel 2007, die Datentypen **XLOPER12** verwenden eingeführt. Mit Ausnahme von **xlAutoFree12**, die Sie in einigen Fällen implementieren müssen, um **XLOPER12** Arbeitsspeicher vermeiden Speicherverlusten können, kann problemlos ausgelassen werden alle die Version 12 **XlAuto** Funktionen, die in diesem Fall ab Excel 2007, Excel Aufrufe der **XLOPER** Versionen. 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel Ruft die [XlAutoOpen](xlautoopen.md) -Funktion, wenn die XLL aktiviert wird. Das Add-In wird aktiviert, am Anfang einer Excel-Sitzung Wenn in der letzten Excel-Sitzung aktiv war, die normalerweise beendet. Das Add-in ist aktiviert, wenn sie während einer Excel-Sitzung geladen wurde. Das Add-in kann deaktiviert und während einer Sitzung Excel erneut aktiviert, und die Funktion für eine erneute Aktivierung aufgerufen wird. 
  
Sie sollten **XlAutoOpen** zum Registrieren von XLL-Funktionen und Befehle, Initialisieren von Datenstrukturen, Anpassen der Benutzeroberfläche und so weiter verwenden. 
  
Wenn Ihr Add-In implementiert und die [XlAutoRegister](xlautoregister-xlautoregister12.md) -Funktion oder die Funktion [xlAutoRegister12 exportiert](xlautoregister-xlautoregister12.md) , versucht Excel möglicherweise, aktivieren und registrieren eine Funktion oder einen Befehl, ohne vorher die **XlAutoOpen** -Funktion. In diesem Fall sollten Sie sicherstellen, dass Ihr Add-in ausreichend für Ihre Funktion oder Befehl ordnungsgemäß initialisiert wird. Wenn sie nicht der Fall ist, sollten Sie entweder beim Registrieren Sie die Funktion oder den Befehl, oder führen Sie die erforderliche Initialisierung fehl. 
  
### <a name="xlautoclose"></a>xlAutoClose

Excel Ruft die [XlAutoClose](xlautoclose.md) -Funktion, wenn die XLL deaktiviert wird. Das Add-In wird deaktiviert werden normalerweise am Ende eine Excel-Sitzung. Wenn der Benutzer während einer Sitzung Excel das Add-in deaktiviert, wird die Funktion aufgerufen. 
  
Verwenden Sie **XlAutoClose** zum Aufheben der Registrierung Funktionen und Befehle, Ressourcen freizugeben, rückgängig Anpassungen und so weiter. 
  
> [!NOTE]
> Es ist ein bekanntes Problem bei der Aufhebung der Registrierung von Funktionen und Befehle. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel Ruft die [XlAutoAdd-Funktion](xlautoadd.md) , wenn der Benutzer die XLL während einer Sitzung Excel aktiviert, mit dem Add-In-Manager. Diese Funktion ist nicht aufgerufen, wenn Excel gestartet und eines vorinstallierten-add-ins lädt. 
  
Sie können diese Funktion verwenden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer teilt mit, dass das Add-In aktiviert wurde, Lese- oder Schreibvorgänge in die Registrierung oder Lizenzinformationen zu überprüfen.
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel Ruft die [XlAutoRemove](xlautoremove.md) -Funktion, wenn der Benutzer mit dem Add-In-Manager die XLL während einer Sitzung Excel deaktiviert. Diese Funktion ist nicht aufgerufen, wenn eine Excel-Sitzung, ordnungsgemäß oder nicht ordnungsgemäß, mit der Add-in installiert wird geschlossen. 
  
Sie können diese Funktion verwenden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer teilt mit, dass das Add-in deaktiviert wurde, oder zum Lesen aus und Schreiben in die Registrierung.
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>XlAddInManagerInfo/xlAddInManagerInfo12

Excel Ruft die [XlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) -Funktion, wenn der Add-In-Manager zum ersten Mal in einer Excel-Sitzung aufgerufen wird. Wenn Excel ein Argument gleich 1 übergibt, sollte eine Zeichenfolge (in der Regel der Name des Add-Ins); dieser Funktion zurückgegeben werden. Es sollte anderenfalls zurückgeben **#VALUE!**.
  
Ab Excel 2007, ruft Excel die Funktion **xlAddInManagerInfo12** anstelle der **XlAddInManagerInfo** -Funktion aus, wenn es von der XLL exportiert wird. Die Funktion **xlAddInManagerInfo12** sollte auf die gleiche Weise wie die **XlAddInManagerInfo** -Funktion zur Vermeidung von versionsspezifischen Unterschiede im Verhalten von XLL funktionieren. Die **xlAddInManagerInfo12** -Funktion sollte einen Datentyp **XLOPER12** zurückgegeben, während die **XlAddInManagerInfo** -Funktion einen Datentyp **XLOPER** zurückgegeben werden soll. 
  
### <a name="xlautoregisterxlautoregister12"></a>XlAutoRegister/xlAutoRegister12

Excel Ruft die [XlAutoRegister](xlautoregister-xlautoregister12.md) -Funktion, wenn ein Anruf an die XLM-Funktion **Registrieren**oder der C-API entsprechende [XlfRegister](xlfregister-form-1.md) -Funktion, mit der Rückgabe vorgenommen wurde und Elementtypen, die für die Funktion registrierende fehlt. Die Funktion **XlAutoRegister** ermöglicht die XLL zum Suchen der internen Liste der exportierten Funktionen und Befehle aus, um die Funktion mit dem Argument registrieren und die angegebenen Typen zurückgegeben. 
  
Ab Excel 2007, ruft Excel die Funktion **xlAddInRegister12** anstelle der **XlAddInRegister** -Funktion aus, wenn es von der XLL exportiert wird. 
  
> [!NOTE]
> Wenn **XlAddInRegister**/ **xlAddInRegister12** versucht, die Funktion ohne das Argument registrieren und Rückgabetypen, eine rekursive Schleife aufrufen auftritt, der schließlich überschreitet die Aufrufliste und festgelegt, dass Excel schließen oder beenden reagiert. 
  
### <a name="xlautofreexlautofree12"></a>XlAutoFree/xlAutoFree12

Excel Ruft die [XlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) -Funktion auf, unmittelbar nachdem eine XLL-Arbeitsblattfunktion einen **XLOPER**gibt/ **XLOPER12** Datentyp mit Kennzeichen, die Excel angewiesen wird, Arbeitsspeicher, die die XLL weiterhin freigegeben werden muss. Auf diese Weise können die XLL zurückzugebenden dynamisch Arrays, Zeichenfolgen und externe Verweise auf das Arbeitsblatt ohne Speicherverluste zugewiesen. Ab Excel 2007, wird der Datentyp **XLOPER12** unterstützt. Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
> [!NOTE]
> Ab Excel 2007, wenn Excel ist multithreaded Arbeitsblatt neu berechnen, die **XlAutoFree**für die Verwendung konfiguriert/ **xlAutoFree12** -Funktion wird aufgerufen, auf dem gleichen Thread, die gerade verwendet wurde, um die Funktion aufgerufen wird, die es zurückgegeben. Der Aufruf von **XlAutoFree**/ **xlAutoFree12** wird immer durchgeführt werden, bevor alle nachfolgenden Arbeitsblattzellen auf diesem Thread ausgewertet werden. Dies vereinfacht die threadsicheren Design in Ihrer XLL. Weitere Informationen finden Sie unter [Multithreaded Neuberechnung in Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Erstellen von XLLs 64-bit

Excel und benutzerdefinierte Funktionen können auf 64-Bit-Betriebssysteme Leistungsvorteile über 32-Bit-Betriebssystemen nutzen ausführen. Excel übergibt Werte in **XLOPER12** Strukturen, die Informationen zu den Typen für die Daten enthalten. Seien Sie vorsichtig bei der Konvertierung zwischen Werten in der Struktur **XLOPER12** und systemeigenen Typen wie **Int** oder Zeiger auf die Werte in der größeren Typ beizubehalten. 
  
## <a name="see-also"></a>Siehe auch



[Anruf XLL-Funktionen aus der Funktions-Assistenten oder Dialogfelder ersetzen](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)
  
[Entwickeln von Excel-XLLs](developing-excel-xlls.md)

