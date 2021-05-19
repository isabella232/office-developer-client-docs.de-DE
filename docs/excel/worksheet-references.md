---
title: Arbeitsblattverweise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- verweise [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
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
  
Ein Verweis in Microsoft Excel ist ein Datentyp, der sich auf einen rechteckigen Zellenblock (bei dem es sich nur um eine Zelle handelt) oder in einigen Fällen auf eine Reihe nicht zusammenschließender Zellenblöcke verweist. Intern verwendet Excel einen Referenztyp für Zellen im aktuellen Blatt, der als interner Verweis bezeichnet wird. Jede Zelle, die sich nicht im aktuellen Blatt befindet, wird durch einen anderen Referenztyp beschrieben, der als externer Verweis bezeichnet wird. Im nächsten Abschnitt finden Sie die Definition von aktiv und aktuell.
  
## <a name="active-vs-current"></a>Aktiv im Vergleich zu Current

In Excel bezieht sich der Begriff aktiv auf das, was der Benutzer anschaut. Die aktive Arbeitsmappe und das Arbeitsblatt sind diejenigen, die der Benutzer derzeit betrachtet, oder, wenn Excel den Fokus auf eine andere Anwendung verloren hat, wurde betrachtet, wann Excel zuletzt den Fokus hatte. Das aktive Blatt befindet sich immer in der aktiven Arbeitsmappe. Die im aktiven Blatt ausgewählten Zellen werden als aktive Zellen bezeichnet. Wenn ein eingebettetes Objekt den Fokus hat, sind die zuletzt ausgewählten Zellen weiterhin aktiv. 
  
Der Begriff current bezieht sich auf das, Excel neu berechnet wird. Die aktuelle Arbeitsmappe und das Aktuelle Arbeitsblatt sind die Arbeitsmappen, die derzeit neu berechnet werden. Das aktuelle Blatt befindet sich immer in der aktuellen Arbeitsmappe. Die neu berechnete Zelle wird als aktuelle Zelle bezeichnet, oder, falls eine Arrayformel neu berechnet wird, die aktuellen Zellen. 
  
Die wichtigsten Punkte, die Sie beachten sollten, sind:
  
- Die aktive Arbeitsmappe/Das Arbeitsblatt/die Zelle ist im Allgemeinen nicht die aktuelle Arbeitsmappe, obwohl dies möglich ist.
    
- Eine Add-In-Funktion, ob in einem Visual Basic for Applications(VBA)-Modul oder einer DLL oder XLL, wird immer aus der aktuellen Zelle des aktuellen Blatts aufgerufen, oder eine von ihnen im Fall der Multithread-Neuberechnung (MTR).
    
Viele Excel, die Informationen zu einer Zelle, einem Zellbereich oder einem Blatt in einer Arbeitsmappe bereitstellen, unterscheiden zwischen der aktiven Arbeitsmappe, dem Blatt oder der Zelle und der aktuellen Arbeitsmappe, dem Blatt oder der aktuellen Zelle. Dieser Unterschied spiegelt sich in den Datentypen wider, die zum Beschreiben von Verweisen auf Zellblöcke verwendet werden, wie im folgenden Abschnitt beschrieben.
  
## <a name="internal-and-external-worksheet-references"></a>Interne und externe Arbeitsblattverweise

Der hauptunterschied zwischen internen und externen Verweisen besteht in dem Externen Referenzdatentyp, der eine ID für das Arbeitsblatt und auch eine Beschreibung der Zellen enthält, auf die verwiesen wird. Ein interner Verweis enthält keinen Verweis auf das Blatt. Es ist implizit, dass es sich bei dem Blatt um das aktuelle Blatt handelt. 
  
Viele C-API-Funktionen geben Verweise zurück oder nehmen Referenzargumente an. Jede C-API-Funktion, die Referenzargumente verwendet, akzeptiert interne oder externe Verweise, mit Ausnahme der **xlSheetNm-Funktion,** die einen externen Verweis erfordert. Einige Funktionen geben nur interne oder externe Verweise zurück. Die C-API-Funktion [xlfCaller](xlfcaller.md) gibt beispielsweise einen Verweis auf die aufrufenden Zellen auf dem aktuellen Blatt per Definition zurück. Der zurückgegebene Verweis ist immer ein interner Verweis, obwohl die Funktion Nichtverweistypen zurückgeben kann, bei denen die Funktion nicht von einer Arbeitsblattzelle aufgerufen wird. Die C-API-Funktion [xlSheetId](xlsheetid.md) gibt immer die ID eines Arbeitsblatts zurück, das in einem externen Referenzdatentyp enthalten ist. 
  
Der andere wichtige Unterschied zwischen den internen und externen Referenztypen ist, dass der externe Referenzdatentyp mehrere nicht miteinander verwobene Zellenblöcke auf demselben Blatt beschreiben kann. Interne Verweise können nur einen einzelnen Block auf dem aktuellen Blatt beschreiben. Nicht ige Verweise können an jede Funktion übergeben werden, die ein Range-Argument verwendet.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel-Arbeitsblatt- und Ausdrucksauswertung](excel-worksheet-and-expression-evaluation.md)

