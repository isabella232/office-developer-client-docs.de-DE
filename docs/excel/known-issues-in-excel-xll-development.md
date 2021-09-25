---
title: Bekannte Probleme in Excel XLL-Entwicklung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Bekannte Probleme [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d44a006802bfbb2e86d04e672253c1ad26a71b1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568173"
---
# <a name="known-issues-in-excel-xll-development"></a>Bekannte Probleme in Excel XLL-Entwicklung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden bekannte Probleme in Microsoft Excel beschrieben, die bei der XLL-Entwicklung auftreten können.
  
## <a name="unregistering-xll-commands-and-functions"></a>Aufheben der Registrierung von XLL-Befehlen und -Funktionen

Wenn eine XLL eine Funktion oder einen Befehl registriert, erstellt Excel einen neuen Namen für die Ressource und ordnet diesem Namen einen Verweis auf die DLL-Funktion zu. Der Name stammt aus dem vierten Argument *pxFunctionText* der [xlfRegister-Funktion.](xlfregister-form-1.md) Dieser Name ist in den normalen Dialogfeldern für die Verwaltung von Arbeitsblattnamen ausgeblendet. Um die Registrierung einer Funktion oder eines Befehls aufzuheben, müssen Sie den Namen mithilfe der [xlfSetName-Funktion](xlfsetname.md) löschen, indem Sie den Namen übergeben, aber keine Definition übergeben. Ein Fehler verhindert jedoch, dass dadurch der Name aus den Listen des Funktions-Assistenten entfernt wird. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Argumentbeschreibung Zeichenfolgenkürzung im Funktions-Assistenten

Der  *Parameter pxArgumentHelp1*  und alle nachfolgenden Parameter der **xlfRegister-Funktion** sind optionale Zeichenfolgen, die den Argumenten der XLL-Funktion entsprechen. Der Funktions-Assistent zeigt diese an, um Hilfe im Dialogfeld "Argumenterstellung" bereitzustellen. Manchmal Excel die Zeichenfolge, die dem letzten Argument entspricht, bei der Anzeige im Dialogfeld um ein oder zwei Zeichen abgeschnitten. Sie können dies vermeiden, indem Sie eine zusätzliche "leere Zeichenfolge" als letzten "Argumenthilfe"-Parameter Ihrer Funktionsregistrierung hinzufügen.
  
## <a name="binary-name-scope-limitation"></a>Einschränkung des Binärnamenbereichs

Binäre Namen und deren Daten können nur abgerufen werden, wenn das Arbeitsblatt, das zum Zeitpunkt der Erstellung aktiv war, wieder aktiv ist. Da Arbeitsblattfunktionen Arbeitsblätter in einer Arbeitsmappe nicht aktivieren können (nur Befehle können dies tun), sind Anwendungen mit binären Namen sehr begrenzt. Wenn Sie beispielsweise über einen Befehl verfügen, der nur aus einem bestimmten Arbeitsblatt aufgerufen wird, können Sie einen binären Namen zum Speichern befehlsbezogener Daten verwenden.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet und Arbeitsmappen mit Arrayformeln

In Excel 2003 und früheren Versionen schlägt die [XlSet-Funktion](xlset.md) fehl, wenn Sie versuchen, einem Bereich in einem Arbeitsblatt, das nicht das aktive Arbeitsblatt ist, Werte zuzuweisen, wobei der entsprechende Bereich auf dem aktiven Blatt eine Arrayformel enthält. In diesem Fall zeigt Excel die Meldung "Sie können einen Teil eines Arrays nicht ändern" an. Dies wurde in Excel 2007 behoben. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Zirkelverweise werden in Datentabellen toleriert

Excel löst derzeit keinen Fehler aus, wenn die Berechnung, auf der eine Datentabelle basiert, auf etwas in der Tabelle selbst verweist. So unwahrscheinlich dieses Szenario auch sein mag, sollten Sie vorsichtig sein, wenn Sie Formeln erstellen oder ändern, die zum Berechnen von Datentabellenwerten verwendet werden.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Konvertieren einer ganzzahligen XLOPER12 in eine XLOPER

Da der ganzzahlige Typ **xltypeInt** eine 32-Bit-Ganzzahl mit Vorzeichen im **XLOPER12-Datentyp** ist, es sich jedoch nur um eine 16-Bit-Ganzzahl mit Vorzeichen im **XLOPER-Datentyp** handelt, ist es möglich, dass einige **XLOPER12-Ganzzahlwerte** nicht in einer ganzzahligen **XLOPER** enthalten sein können. Wenn Excel diesen Typ intern konvertiert, wird dieses Problem behoben, indem der Typ in einen **XltypeNum** XLOPER-Gleitkommawert konvertiert **wird.**
  
Die Framework [XLOper12ToXLOper-Funktion](xloper12toxloper.md) spiegelt dieses Verhalten wider, um intern mit Excel konsistent zu sein. Wenn Sie diese Funktion aufrufen, sollten Sie nicht davon ausgehen, dass der zurückgegebene **XLOPER** immer **xltypeInt** ist; beim Lesen **my_xloper.val.w** wird ein falscher Wert zurückgegeben, wenn der **my_xloper** Typ **xltypeNum** ist.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Zurückgeben von XLOPER oder XLOPER12 durch Ändern vorhandener Argumente

Excel ermöglicht die Registrierung von Funktionen, die einen XLOPER oder **XLOPER12** zurückgeben, indem ein vorhandenes Argument geändert wird.  Wenn jedoch ein **XLOPER** /  **XLOPER12-Argument** auf den Speicher zeigt und der Zeiger dann durch den Rückgabewert der DLL-Funktion überschrieben wird, kann Excel Arbeitsspeicher freigeben. Excel zeigt keinen Fehler an, kann aber schließlich abstürzt. Wenn die DLL Speicher für den Rückgabewert zugewiesen hat, versuchen Excel möglicherweise, diesen Speicher freizugeben, was zu einem sofortigen Anwendungsabstürzen führen kann. Daher sollten Sie **XLOPER** /  **XLOPER12-Argumente** nicht direkt ändern. Alle **XLOPER-** oder **XLOPER12-Argumente** sollten als streng schreibgeschützt behandelt werden. 
  
Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Siehe auch



[XLOper12ToXLOper](xloper12toxloper.md)


[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)
  
[Speicherverwaltung in Excel](memory-management-in-excel.md)

