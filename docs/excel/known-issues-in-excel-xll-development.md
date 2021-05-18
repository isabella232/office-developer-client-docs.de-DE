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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304004"
---
# <a name="known-issues-in-excel-xll-development"></a>Bekannte Probleme in Excel XLL-Entwicklung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In diesem Thema werden bekannte Probleme in Microsoft Excel beschrieben, die bei der XLL-Entwicklung auftreten können.
  
## <a name="unregistering-xll-commands-and-functions"></a>Aufheben der Registrierung von XLL-Befehlen und -Funktionen

Wenn eine XLL eine Funktion oder einen Befehl registriert, erstellt Excel einen neuen Namen für die Ressource und ordnet diesem Namen einen Verweis auf die DLL-Funktion zu. Der Name wird aus dem vierten Argument  *pxFunctionText*  der [xlfRegister-Funktion](xlfregister-form-1.md) übernommen. Dieser Name wird in den normalen Dialogfelder zum Verwalten von Arbeitsblattnamen ausgeblendet. Wenn Sie die Registrierung einer Funktion oder eines Befehls aufheben möchten, müssen Sie den Namen mithilfe der [xlfSetName-Funktion](xlfsetname.md) löschen, indem Sie den Namen übergeben, aber keine Definition übergeben. Ein Fehler verhindert jedoch, dass der Name aus den Listen des #A0 entfernt wird. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Argumentbeschreibung Zeichenfolgenkürzung im Funktions-Assistenten

Der  *Parameter pxArgumentHelp1*  und alle nachfolgenden Parameter der **xlfRegister-Funktion** sind optionale Zeichenfolgen, die den Argumenten der XLL-Funktion entsprechen. Der Funktions-Assistent zeigt diese an, um Hilfe im Dialogfeld Argumentkonstruktion zu bieten. Manchmal Excel die Zeichenfolge, die dem letzten Argument entspricht, beim Anzeigen im Dialogfeld um ein oder zwei Zeichen abgeschnitten. Sie können dies vermeiden, indem Sie eine zusätzliche leere Zeichenfolge als letzten Parameter für die Argumenthilfe ihrer Funktionsregistrierung hinzufügen.
  
## <a name="binary-name-scope-limitation"></a>Einschränkung des Binärnamenbereichs

Binäre Namen und ihre Daten können nur abgerufen werden, wenn das Arbeitsblatt, das zum Zeitpunkt der Erstellen aktiv war, wieder aktiv ist. Da Arbeitsblattfunktionen Arbeitsblätter in einer Arbeitsmappe nicht aktivieren können (nur Befehle können dies tun), sind Anwendungen mit binären Namen sehr begrenzt. Wenn Sie über einen Befehl verfügen, der nur von einem bestimmten Arbeitsblatt aufgerufen wird, können Sie beispielsweise einen binären Namen verwenden, um befehlsbezogene Daten zu speichern.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet und Arbeitsmappen mit Arrayformeln

In Excel 2003 und früheren Versionen schlägt die [xlSet-Funktion](xlset.md) fehl, wenn Sie versuchen, einem Bereich in einem Arbeitsblatt, das nicht das aktive Arbeitsblatt ist, Werte zuzuordnen, wobei der entsprechende Bereich im aktiven Blatt eine Arrayformel enthält. In diesem Fall Excel die Meldung "Sie können einen Teil eines Arrays nicht ändern". Dies wurde in Excel 2007 behoben. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Zirkelverweise werden in Datentabellen toleriert

Excel verursacht derzeit keinen Fehler, wenn die Berechnung, auf der eine Datentabelle basiert, auf etwas in der Tabelle selbst verweist. So unwahrscheinlich dieses Szenario auch sein mag, Sie sollten beim Erstellen oder Ändern von Formeln, die zum Berechnen von Datentabellewerten verwendet werden, vorsichtig sein.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Konvertieren einer ganzzahligen XLOPER12 in einen XLOPER

Da der ganzzahlige Typ **xltypeInt** eine 32-Bit-ganze Zahl im **XLOPER12-Datentyp** ist, es sich jedoch nur um eine 16-Bit-ganzzahlige Zahl im **XLOPER-Datentyp** handelt, können einige ganzzahlige **XLOPER12-Werte** nicht in einer ganzzahligen **XLOPER enthalten sein.** Wenn Excel diesen Typ intern konvertiert, wird dieses Problem dadurch behoben, dass der Typ in einen Gleitkommatyp **xltypeNum** **XLOPER konvertiert wird.**
  
Die Framework [XLOper12ToXLOper-Funktion](xloper12toxloper.md) spiegelt dieses Verhalten so ab, dass es intern Excel ist. Wenn Sie diese Funktion aufrufen, sollten Sie nicht davon ausgehen, dass der zurückgegebene **XLOPER** immer **xltypeInt ist.** Das **my_xloper.val.w** gibt einen false-Wert an, wenn der **my_xloper** **xltypeNum ist.**
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Zurückgeben von XLOPER oder XLOPER12 durch Ändern von Argumenten an Ort und Stelle

Excel ermöglicht die Registrierung von Funktionen, die einen **XLOPER-** oder **XLOPER12-Wert** zurückgeben, indem ein vorhandenes Argument geändert wird. Wenn jedoch ein **XLOPER** /  **XLOPER12-Argument** auf den Arbeitsspeicher verweist und der Zeiger dann vom Rückgabewert der DLL-Funktion überschrieben wird, Excel Speicher verloren. Excel wird kein Fehler angezeigt, aber es kann schließlich abstürzen. Wenn die DLL den Arbeitsspeicher für den Rückgabewert zugewiesen hat, Excel möglicherweise versuchen, diesen Speicher frei zu geben, was zu einem sofortigen Anwendungsabsturz führen kann. Daher sollten Sie **xlOPER** /  **XLOPER12-Argumente nicht** an Ort und Stelle ändern. Alle **XLOPER-** oder **XLOPER12-Argumente** sollten als streng schreibgeschützt behandelt werden. 
  
Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Siehe auch



[XLOper12ToXLOper](xloper12toxloper.md)


[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)
  
[Speicherverwaltung in Excel](memory-management-in-excel.md)

