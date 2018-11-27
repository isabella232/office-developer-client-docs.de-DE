---
title: Bekannte Probleme in Excel XLL-Entwicklung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Bekannte Probleme [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: f139451a43598b59da22775333779df691df460a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2018
ms.locfileid: "26685179"
---
# <a name="known-issues-in-excel-xll-development"></a>Bekannte Probleme in Excel XLL-Entwicklung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden bekannte Probleme in Microsoft Excel, die bei der Entwicklung von XLL auftreten können.
  
## <a name="unregistering-xll-commands-and-functions"></a>Aufheben der Registrierung von XLL-Befehle und Funktionen

Wenn eine XLL eine Funktion oder einen Befehl registriert, Excel erstellt einen neuen Namen für die Ressource und einen Verweis auf die DLL-Funktion mit diesem Namen. Der Name wird aus dem vierten Argument, *PxFunctionText* der Funktion [XlfRegister](xlfregister-form-1.md) übernommen. Dieser Name ist die normale Dialogfelder für die Verwaltung von Arbeitsblattnamen ausgeblendet. Um eine Funktion oder einen Befehl Aufheben der Registrierung, müssen Sie den Namen durch Verwenden der Funktion [XlfSetName](xlfsetname.md) , übergeben Sie den Namen, aber nicht übergeben eine Definition löschen. Dies verhindert jedoch ein Fehler aus den Listen Funktions-Assistenten den Namen entfernt. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Argument Beschreibung Zeichenfolge abschneiden im Funktions-Assistenten

Der Parameter *pxArgumentHelp1* und alle nachfolgenden Parameter der Funktion **XlfRegister** sind optional Zeichenfolgen, die die Argumente der XLL-Funktion entsprechen. Funktions-Assistent zeigt diese um Hilfe im Dialogfeld Argument Konstruktion bereitzustellen. In einigen Fällen schneidet Excel die Zeichenfolge, die zum letzten Argument durch ein oder zwei Zeichen entspricht, in dem Dialogfeld angezeigt. Sie können dies vermeiden, indem eine zusätzliche "leere Zeichenfolge" als letzter "Argument Hilfe" Parameter Ihrer Funktion Registrierung hinzufügen.
  
## <a name="binary-name-scope-limitation"></a>Binäre Name Bereich Einschränkung

Nur, wenn das Arbeitsblatt, das aktiv gleichzeitig war, den sie erstellt wurden, erneut aktiv ist, können Binary Namen und ihre Daten abgerufen werden. Da Microsoft Excel-Arbeitsblattfunktionen können nicht aktivieren Arbeitsblätter in einer Arbeitsmappe (nur Befehle möglich), Anwendungen von binären Namen sind sehr begrenzt. Wenn Sie einen Befehl, der nur ein bestimmtes Arbeitsblatt aufgerufen wird verfügen, beispielsweise können einen binären Namen Sie Daten im Zusammenhang mit dem Befehl speichern.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>gleich XlSet und Arbeitsmappen mit Arrayformeln

In Excel 2003 und früheren Versionen fällt aus der [gleich XlSet-Funktion](xlset.md) , wenn Sie versuchen, einen Bereich in einem Arbeitsblatt Werte zuweisen, die nicht im aktiven Arbeitsblatt ist, bei denen der entsprechende Bereich im aktiven Blatt eine Arrayformel enthält. In diesem Fall Meldung Excel die "Sie Teil einer Arrayformel ändern können." Dies wurde in Excel 2007 behoben. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Zirkelverweise werden in Datentabellen vorgenommen.

Excel derzeit kein Fehler ausgelöst sich die Berechnung, der eine Datentabelle basiert auf etwas in der Tabelle selbst bezieht. Wie unwahrscheinlich, wie in diesem Szenario werden kann, sollten Sie vorsichtig beim Erstellen oder Ändern von Formeln, die zum Berechnen von Datenwerten-Tabelle verwendet werden.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Konvertieren von XLOPER12 ganze Zahl in eine XLOPER

Da die ganze Zahl Typ **vom Typ XltypeInt** eine 32-Bit-Ganzzahl mit Vorzeichen in den Datentyp **XLOPER12 ist** , aber es nur eine 16-Bit-Ganzzahl mit Vorzeichen in den Datentyp **XLOPER ist** , ist es möglich, dass einige Werte für ganze Zahl **XLOPER12** können, in enthalten sein eine ganze Zahl **XLOPER**. Ruft, in denen Excel intern dieses Typs konvertiert, indem Konvertieren des Typs in eine Gleitkommazahl **XltypeNum** **XLOPER**dieses Problem umgehen.
  
Die Funktion Framework [XLOper12ToXLOper](xloper12toxloper.md) spiegelt dieses Verhalten, um mit Excel intern übereinstimmen. Wenn Sie diese Funktion aufrufen, sollten Sie nicht davon ausgehen, dass die zurückgegebene **XLOPER** immer **vom Typ XltypeInt**ist; Lesen von **my_xloper.val.w** liefert Wert false, wenn der Typ **My_xloper** **XltypeNum**ist.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Zurückgeben von XLOPER oder XLOPER12 durch Bearbeiten der Argumente direkten

Excel ermöglicht die Registrierung von Funktionen, die ein **XLOPER** oder **XLOPER12** durch Ändern der direkten Argument zurückgeben. Jedoch, wenn eine **XLOPER**/ **XLOPER12** Argument Kriterien, Arbeitsspeicher und der Mauszeiger wird durch den Rückgabewert der DLL-Funktion dann überschrieben, Excel kann es zu Speicherverlusten. Wird einen Fehler in Excel nicht angezeigt, aber es kann schließlich abstürzen. Wenn die DLL für den Rückgabewert Speicher belegt, möglicherweise auch Excel versuchen, diesen Speicher freizugeben, der zum Absturz der Anwendung sofortige verursachen können. Aus diesem Grund sollten Sie nicht **XLOPER**ändern/ **XLOPER12** Argumente vorhanden. Alle **XLOPER** oder **XLOPER12** Argumente sollte als streng schreibgeschützt behandelt werden. 
  
Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Siehe auch



[XLOper12ToXLOper](xloper12toxloper.md)


[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)
  
[Speicherverwaltung in Excel](memory-management-in-excel.md)

