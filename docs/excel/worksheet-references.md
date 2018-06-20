---
title: Arbeitsblatt-Verweise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Verweise [excel 2007], Arbeitsblatt, Arbeitsblatt Verweise [Excel 2007], externe Arbeitsblatt Verweise [Excel 2007], aktiven Arbeitsblatt [Excel 2007], aktuelle Arbeitsblatt [Excel 2007], interne Arbeitsblatt verweist [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790589"
---
# <a name="worksheet-references"></a>Arbeitsblatt-Verweise

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ein Verweis in Microsoft Excel ist ein Datentyp, der auf einen rechteckigen Block von Zellen (die nur eine Zelle sein können) oder in einigen Fällen eine Anzahl von nicht zusammenhängenden Blöcke mit Zellen verweist. Intern verwendet Excel eine Verweistyp für Zellen auf das aktuelle Blatt, das als einen internen Verweis bezeichnet. Eine beliebige Zelle, die nicht auf das aktuelle Blatt ist wird durch einen anderen Typ als ein externer Verweis bezeichnet Referenz beschrieben. Finden Sie im nächsten Abschnitt für die Definition der aktive und aktuelle.
  
## <a name="active-vs-current"></a>Im Vergleich zu aktuellen aktiven

In Excel bezieht sich der Begriff active, was dem Benutzer angezeigt wird. Der aktiven Arbeitsmappe und dem Arbeitsblatt, sind die, die der Benutzer derzeit betrachten, oder, wenn Excel den Fokus zu einer anderen Anwendung verloren hat wurde betrachten bei Excel zuletzt den Fokus hatte. Das aktive Blatt ist immer in der aktiven Arbeitsmappe. Eine oder mehrere Zellen, die in dem aktiven Blatt ausgewählt sind, werden als aktiven Zellen bezeichnet. Wenn ein eingebettetes Objekt den Fokus besitzt, sind die zuletzt ausgewählte Zellen noch aktiv. 
  
Der aktuellen Ausdruck verweist auf was Excel neu berechnet. Der aktuellen Arbeitsmappe und dem Arbeitsblatt, sind die, die derzeit neu berechnet werden. Das aktuelle Blatt ist immer in der aktuellen Arbeitsmappe. Die Zelle neu berechnet wird als die aktuelle Zelle oder im Fall einer Arrayformel neu berechnet wird, den aktuellen Zellen bezeichnet. 
  
Wichtige Punkte zu berücksichtigen sind wie folgt:
  
- Die aktive Arbeitsmappe / / Arbeitsblattzelle ist nicht in der Regel der aktuellen Unterhaltung, obwohl es möglich ist.
    
- Eine Funktion-Add-in wird, ob in einem Visual Basic für Applikationen (VBA) Modul oder eine DLL oder XLL, immer von der aktuellen Zelle auf das aktuelle Blatt oder in einer von ihnen im Fall von Multithread-neuberechnung (MTR) aufgerufen.
    
Viele Funktionen von Excel, die Informationen über eine Zelle, einen Bereich von Tabellenzellen oder einem Blatt in einer Arbeitsmappe enthalten unterscheiden zwischen der aktiven Arbeitsmappe, Blatt, oder Zelle und die aktuelle Arbeitsmappe, Blatt oder das Zelle. Diesen Unterschied wiedergegeben wird in den Datentypen verwendet, um Verweise auf Zellblöcke wird beschrieben, wie im folgenden Abschnitt beschrieben.
  
## <a name="internal-and-external-worksheet-references"></a>Arbeitsblatt für interne und externe Verweise

Der wesentliche Unterschied zwischen internen und externen Verweise ist, dass der externen Daten Verweistyp enthält eine ID für das Arbeitsblatt und auch eine Beschreibung der Zellen auf die verwiesen werden. Ein interner Verweis enthält keinen Verweis auf das Blatt – es ist implizit, dass das Blatt das aktuelle Blatt ist. 
  
Viele Funktionen der C-API Verweise zurückgeben oder Verweis Argumente. Eine beliebige C-API-Funktion nimmt Argumente verweisen akzeptiert Verweise auf intern oder extern, mit Ausnahme der **XlSheetNm** -Funktion, die einen externen Verweis erforderlich sind. Einige Funktionen zurückgeben nur intern oder extern Verweise. Beispielsweise gibt einen Verweis auf die aufrufenden Zellen mit der C-API-Funktion [XlfCaller](xlfcaller.md) per Definition auf das aktuelle Blatt zurück. Der zurückgegebene Verweis ist immer ein interner Verweis, zwar die Funktion nicht Verweis-zurückzugeben, in dem die Funktion nicht aus einer Arbeitsblattzelle aufgerufen. Der C-API-Funktion [XlSheetId](xlsheetid.md) gibt immer die ID eines Arbeitsblatts in ein externer Verweisdatentyp enthaltenen zurück. 
  
Der wesentliche Unterschied zwischen den internen und externen Verweistypen ist, dass der Datentyp externer Bezug mehrere Zellen eines nicht zusammenhängenden Blöcke auf demselben Blatt beschreiben kann. Interne Verweise können nur einen einzelnen Block auf das aktuelle Blatt beschreiben. Nicht zusammenhängenden Verweise können auf jede Funktion übergeben werden, die ein Range-Argument akzeptiert.
  
## <a name="see-also"></a>Siehe auch



[Excel-Programmierkonzepte](excel-programming-concepts.md)
  
[Auswerten von Namen und andere Arbeitsblatt Formula-Ausdr�cke](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel-Arbeitsblatt und die Auswertung von Ausdrücken](excel-worksheet-and-expression-evaluation.md)

