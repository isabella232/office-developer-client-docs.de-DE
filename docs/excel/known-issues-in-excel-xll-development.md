---
title: Bekannte Probleme in Excel XLL-Entwicklung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Bekannte Probleme [Excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304004"
---
# <a name="known-issues-in-excel-xll-development"></a>Bekannte Probleme in Excel XLL-Entwicklung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden bekannte Probleme in Microsoft Excel beschrieben, die bei der XLL-Entwicklung auftreten können.
  
## <a name="unregistering-xll-commands-and-functions"></a>Aufheben der Registrierung von XLL-Befehlen und-Funktionen

Wenn eine XLL eine Funktion oder einen Befehl registriert, erstellt Excel einen neuen Namen für die Ressource und ordnet einen Verweis auf die DLL-Funktion mit diesem Namen zu. Der Name stammt aus dem vierten Argument, *pxFunctionText* , der [xlfRegister](xlfregister-form-1.md) -Funktion. Dieser Name wird in den normalen Dialogfeldern für die Verwaltung von Arbeitsblattnamen ausgeblendet. Zum Aufheben der Registrierung einer Funktion oder eines Befehls müssen Sie den Namen mithilfe der [xlfSetName](xlfsetname.md) -Funktion löschen, wobei Sie den Namen übergeben, jedoch keine Definition übergeben. Ein Fehler verhindert jedoch, dass der Name aus den Listen des Funktions-Assistenten entfernt wird. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Argument Beschreibung string TRUNCATE im Function Wizard

Der *pxArgumentHelp1* -Parameter und alle nachfolgenden Parameter der **xlfRegister** -Funktion sind optionale Zeichenfolgen, die den Argumenten der XLL-Funktion entsprechen. Der Funktions-Assistent zeigt diese Informationen an, um Hilfe im Dialogfeld "Argument Erstellung" zu erhalten. Manchmal schneidet Excel die Zeichenfolge, die dem letzten Argument entspricht, mit einem oder zwei Zeichen ab, wenn Sie im Dialogfeld angezeigt wird. Sie können dies vermeiden, indem Sie eine zusätzliche leere Zeichenfolge als letzten "Argument Hilfe"-Parameter Ihrer Funktions Registrierung hinzufügen.
  
## <a name="binary-name-scope-limitation"></a>Beschränkung des binären Namensbereichs

Binäre Namen und Ihre Daten können nur abgerufen werden, wenn das Arbeitsblatt, das zum Zeitpunkt der Erstellung aktiv war, wieder aktiv ist. Da Arbeitsblattfunktionen Arbeitsblätter in einer Arbeitsmappe nicht aktivieren können (Dies kann nur mit Befehlen ausgeführt werden), sind Anwendungen mit binären Namen sehr eingeschränkt. Wenn Sie einen Befehl haben, der nur von einem bestimmten Arbeitsblatt aus aufgerufen wird, können Sie beispielsweise einen binären Namen verwenden, um Befehls bezogene Daten zu speichern.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet und Arbeitsmappen mit Array Formeln

In Excel 2003 und früheren Versionen schlägt die [xlSet-Funktion](xlset.md) fehl, wenn Sie versuchen, einem Bereich in einem Arbeitsblattwerte zuzuweisen, bei dem es sich nicht um das aktive Arbeitsblatt handelt, wobei der entsprechende Bereich im aktiven Blatt eine Arrayformel enthält. In diesem Fall zeigt Excel die Meldung "Sie können einen Teil eines Arrays nicht ändern" aus. Dies wurde in Excel 2007 behoben. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Zirkelbezüge werden in Datentabellen toleriert

Excel löst derzeit keinen Fehler aus, wenn die Berechnung, auf der eine Datentabelle basiert, auf etwas in der Tabelle selbst verweist. Bei diesem Szenario sollten Sie beim Erstellen oder Ändern von Formeln, die zum Berechnen von Datentabellen Werten verwendet werden, vorsichtig sein.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Konvertieren einer ganzzahligen XLOPER12 in ein XLOPER

Da der ganzzahlige Typ **xltypeInt** eine 32-Bit-Ganzzahl mit Vorzeichen im **XLOPER12** -Datentyp ist, aber es ist nur eine 16-Bit-Ganzzahl mit Vorzeichen im **XLOPER** -Datentyp, ist es möglich, dass einige ganzzahlige **XLOPER12** -Werte nicht in einer Integer- **XLOPER**. Wenn dieser Typ von Excel intern konvertiert wird, wird dieses Problem durch Konvertieren des Typs in eine Gleitkomma- **xltypeNum** **XLOPER**.
  
Die Framework- [XLOper12ToXLOper](xloper12toxloper.md) -Funktion spiegelt dieses Verhalten als konsistent mit Excel intern wider. Wenn Sie diese Funktion aufrufen, sollten Sie nicht davon ausgehen, dass die zurückgegebene **XLOPER** immer **xltypeInt**wird; das Lesen von **my_xloper. Val. w** gibt einen false-Wert an, wenn der **My_xloper** -Typ **xltypeNum**ist.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Zurückgeben von XLOPER oder XLOPER12 durch Ändern von Argumenten

Excel ermöglicht die Registrierung von Funktionen, die ein **XLOPER** oder **XLOPER12** zurückgeben, indem Sie ein direktes Argument ändern. Wenn jedoch ein **XLOPER**/ -**XLOPER12** -Argument auf den Arbeitsspeicher zeigt und der Zeiger dann durch den Rückgabewert der DLL-Funktion überschrieben wird, kann Excel Speicher auslaufen. In Excel wird kein Fehler angezeigt, aber möglicherweise stürzt es schließlich ab. Wenn der DLL-Speicher für den Rückgabewert reserviert wurde, versucht Excel auch, diesen Speicher zu befreien, was zu einem unmittelbaren Anwendungsabsturz führen kann. Daher sollten Sie **XLOPER**/ **XLOPER12** -Argumente nicht direkt ändern. Alle **XLOPER** -oder **XLOPER12** -Argumente sollten als streng schreibgeschützt behandelt werden. 
  
Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Siehe auch



[XLOper12ToXLOper](xloper12toxloper.md)


[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)
  
[Speicherverwaltung in Excel](memory-management-in-excel.md)

