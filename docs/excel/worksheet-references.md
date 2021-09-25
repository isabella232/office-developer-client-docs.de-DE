---
title: Arbeitsblattverweise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ddc0c2d1c1dc88e68e51ac7843b990a926244920
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557617"
---
# <a name="worksheet-references"></a>Arbeitsblattverweise

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ein Bezug in Microsoft Excel ist ein Datentyp, der sich auf einen rechteckigen Zellenblock (der nur eine Zelle sein kann) oder in einigen Fällen auf eine Reihe von nicht zusammenhängenden Zellblöcken bezieht. Intern verwendet Excel einen Bezugstyp für Zellen auf dem aktuellen Blatt, der als interner Bezug bezeichnet wird. Jede Zelle, die sich nicht auf dem aktuellen Blatt befindet, wird durch einen anderen Verweistyp beschrieben, der als externer Bezug bezeichnet wird. Die Definition von "Aktiv" und "Aktuell" finden Sie im nächsten Abschnitt.
  
## <a name="active-vs-current"></a>Aktiv im Vergleich zur aktuellen

In Excel bezieht sich der Begriff "aktiv" auf das, was der Benutzer anzeigt. Die aktive Arbeitsmappe und das aktive Arbeitsblatt sind dieJenigen, die der Benutzer gerade betrachtet oder, wenn Excel den Fokus auf eine andere Anwendung verloren hat, sich ansieht, wann Excel zuletzt den Fokus hatte. Das aktive Blatt befindet sich immer in der aktiven Arbeitsmappe. Die im aktiven Blatt ausgewählten Zellen werden als aktive Zellen bezeichnet. Wenn ein eingebettetes Objekt den Fokus hat, sind die zuletzt ausgewählten Zellen weiterhin aktiv. 
  
Der Begriff "aktuell" bezieht sich auf das, was Excel neu berechnet. Die aktuelle Arbeitsmappe und das aktuelle Arbeitsblatt werden gerade neu berechnet. Das aktuelle Blatt befindet sich immer in der aktuellen Arbeitsmappe. Die neu berechnete Zelle wird als aktuelle Zelle bezeichnet, oder im Falle einer neu berechneten Arrayformel die aktuellen Zellen. 
  
Beachten Sie folgende wichtige Punkte:
  
- Die aktive Arbeitsmappe/das aktive Arbeitsblatt/die aktive Zelle ist im Allgemeinen nicht die aktuelle, obwohl dies möglich ist.
    
- Eine Add-In-Funktion, sei es in einem Visual Basic for Applications(VBA)-Modul oder einer DLL oder XLL, wird immer aus der aktuellen Zelle des aktuellen Blatts aufgerufen, oder eine dieser Funktionen bei multithreaded recalculation (MTR).
    
Viele Excel Funktionen, die Informationen zu einer Zelle, einem Zellbereich oder einem Blatt in einer Arbeitsmappe bereitstellen, unterscheiden zwischen der aktiven Arbeitsmappe, dem aktiven Blatt oder der aktiven Zelle und der aktuellen Arbeitsmappe, dem aktuellen Blatt oder der aktuellen Zelle. Dieser Unterschied spiegelt sich in den Datentypen wider, die zum Beschreiben von Verweisen auf Zellblöcke verwendet werden, wie im folgenden Abschnitt beschrieben.
  
## <a name="internal-and-external-worksheet-references"></a>Interne und externe Arbeitsblattverweise

Der Hauptunterschied zwischen internen und externen Verweisen besteht darin, dass der externe Verweisdatentyp eine ID für das Arbeitsblatt sowie eine Beschreibung der Zellen enthält, auf die verwiesen wird. Ein interner Verweis enthält keinen Verweis auf das Blatt– es ist implizit, dass es sich bei dem Blatt um das aktuelle Blatt handelt. 
  
Viele C-API-Funktionen geben Verweise zurück oder verwenden Referenzargumente. Jede C-API-Funktion, die Referenzargumente akzeptiert, akzeptiert interne oder externe Verweise, mit Ausnahme der **XlSheetNm-Funktion,** die einen externen Verweis erfordert. Einige Funktionen geben nur interne oder externe Verweise zurück. Beispielsweise gibt die C-API-Funktion [xlfCaller](xlfcaller.md) einen Verweis auf die aufrufenden Zellen per Definition auf dem aktuellen Blatt zurück. Der zurückgegebene Verweis ist immer ein interner Verweis, obwohl die Funktion Nicht-Verweistypen zurückgeben kann, bei denen die Funktion nicht aus einer Arbeitsblattzelle aufgerufen wird. Die C-API-Funktion [xlSheetId](xlsheetid.md) gibt immer die ID eines Arbeitsblatts zurück, das in einem externen Verweisdatentyp enthalten ist. 
  
Der andere Hauptunterschied zwischen dem internen und externen Verweistyp besteht darin, dass der externe Verweisdatentyp mehrere nicht zusammenhängenden Zellblöcke auf demselben Blatt beschreiben kann. Interne Verweise können nur einen einzelnen Block auf dem aktuellen Blatt beschreiben. Getrennte Verweise können an jede Funktion übergeben werden, die ein Bereichsargument verwendet.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel-Arbeitsblatt- und Ausdrucksauswertung](excel-worksheet-and-expression-evaluation.md)

