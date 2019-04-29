---
title: Arbeitsblattverweise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Referenzen [Excel 2007], Arbeitsblatt, Arbeitsblatt Referenzen [Excel 2007], Verweise auf externe Arbeitsblätter [Excel 2007], aktives Arbeitsblatt [Excel 2007], Aktuelles Arbeitsblatt [Excel 2007], interne Arbeitsblatt Referenzen [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416461"
---
# <a name="worksheet-references"></a>Arbeitsblattverweise

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ein Verweis in Microsoft Excel ist ein Datentyp, der auf einen rechteckigen Zellenblock (der nur eine Zelle sein kann) oder in einigen Fällen eine Reihe von nicht zusammenhängenden Zellen Blöcken verweist. Intern verwendet Excel einen Verweistyp für Zellen im aktuellen Blatt, der als interne Referenz bezeichnet wird. Jede Zelle, die sich nicht im aktuellen Blatt befindet, wird durch einen anderen Verweistyp beschrieben, der als externe Referenz bezeichnet wird. Weitere Informationen finden Sie im nächsten Abschnitt für die Definition von aktiv und aktuell.
  
## <a name="active-vs-current"></a>Aktiv vs. Current

In Excel bezieht sich der Begriff Active auf das, was der Benutzer anzeigt. Die aktive Arbeitsmappe und das Arbeitsblatt sind diejenigen, die der Benutzer derzeit ansieht, oder, wenn Excel den Fokus auf eine andere Anwendung verloren hat, wenn Excel zuletzt den Fokus hatte. Das aktive Blatt befindet sich immer in der aktiven Arbeitsmappe. Die Zellen, die im aktiven Blatt ausgewählt sind, werden als aktive Zellen bezeichnet. Wenn ein eingebettetes Objekt den Fokus besitzt, sind die zuletzt ausgewählten Zellen weiterhin aktiv. 
  
Der Begriff Current bezieht sich auf das, was Excel neu berechnet. Die aktuelle Arbeitsmappe und das Arbeitsblatt sind diejenigen, die derzeit neu berechnet werden. Das aktuelle Blatt befindet sich immer in der aktuellen Arbeitsmappe. Die neu berechnete Zelle wird als aktuelle Zelle oder, im Fall einer neu berechneten Arrayformel, der aktuellen Zellen bezeichnet. 
  
Die wichtigsten Punkte, die Sie sich merken sollten, sind wie folgt:
  
- Die aktive Arbeitsmappe/das Arbeitsblatt/die Zelle ist im Allgemeinen nicht die aktuelle, obwohl dies der Fall sein kann.
    
- Eine Add-in-Funktion, unabhängig davon, ob Sie in einem VBA-Modul (Visual Basic für Applikationen) oder in einer DLL oder XLL ausgeführt wird, wird immer aus der aktuellen Zelle des aktuellen Blatts oder einer von Ihnen im Fall von Multithread-Neuberechnung (MTR) aufgerufen.
    
Viele Excel-Funktionen, die Informationen zu einer Zelle, einem Zellbereich oder einem Blatt in einer Arbeitsmappe bereitstellen, unterscheiden zwischen der aktiven Arbeitsmappe, dem Blatt oder der Zelle und der aktuellen Arbeitsmappe, des Blatts oder der Zelle. Dieser Unterschied spiegelt sich in den Datentypen wider, die zum Beschreiben von Verweisen auf Zellenblöcke verwendet werden, wie im folgenden Abschnitt beschrieben.
  
## <a name="internal-and-external-worksheet-references"></a>Interne und externe Arbeitsblattverweise

Der wesentliche Unterschied zwischen internen und externen verweisen besteht darin, dass der externe Referenz Datentyp eine ID für das Arbeitsblatt enthält und auch eine Beschreibung davon, auf welche Zellen verwiesen wird. Ein interner Verweis enthält keinen Verweis auf das Blatt, es ist implizit, dass das Blatt das aktuelle Blatt ist. 
  
Viele C-API-Funktionen geben Verweise zurück oder verweisen auf Argumente. Jede C-API-Funktion, die Verweisargumente verwendet, akzeptiert interne oder externe Verweise, mit Ausnahme der **xlSheetNm** -Funktion, die einen externen Verweis erfordert. Einige Funktionen geben nur interne oder externe Verweise zurück. Beispielsweise gibt die C-API-Funktion [xlfCaller](xlfcaller.md) einen Verweis auf die aufrufenden Zellen im aktuellen Blatt per Definition zurück. Der zurückgegebene Verweis ist immer ein interner Verweis, obwohl die Funktion nicht-Verweistypen zurückgeben kann, bei denen die Funktion nicht von einer Arbeitsblattzelle aus aufgerufen wird. Die C-API-Funktion [xlSheetId](xlsheetid.md) gibt immer die ID eines Arbeitsblatts zurück, das in einem externen Verweisdatentyp enthalten ist. 
  
Der andere wesentliche Unterschied zwischen den internen und externen Verweistypen besteht darin, dass der externe Referenz Datentyp mehrere nicht zusammenhängende Zellenblöcke auf demselben Blatt beschreiben kann. Interne Verweise können nur einen einzelnen Block im aktuellen Blatt beschreiben. Nicht zusammenhängende Verweise können an eine beliebige Funktion übergeben werden, die ein Range-Argument akzeptiert.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel-Arbeitsblatt- und Ausdrucksauswertung](excel-worksheet-and-expression-evaluation.md)

