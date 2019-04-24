---
title: LIKE (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Bestimmt, ob eine bestimmte Zeichenfolge mit einem angegebenen Muster übereinstimmt. Ein Muster kann reguläre Zeichen und Platzhalterzeichen enthalten. Während des Mustervergleichs müssen reguläre Zeichen genau mit den in der Zeichenfolge angegebenen Zeichen übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Fragmenten der Zeichenfolge abgeglichen werden. Durch die Verwendung von Platzhalterzeichen wird der LIKE-Operator flexibler als die Verwendung der Zeichenfolgenvergleichs Operatoren = und!.
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311081"
---
# <a name="like-access-custom-web-app"></a>LIKE (Access Custom Web App)

Bestimmt, ob eine bestimmte Zeichenfolge mit einem angegebenen Muster übereinstimmt. Ein Muster kann reguläre Zeichen und Platzhalterzeichen enthalten. Während des Mustervergleichs müssen reguläre Zeichen genau mit den in der Zeichenfolge angegebenen Zeichen übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Fragmenten der Zeichenfolge abgeglichen werden. Durch die Verwendung von Platzhalterzeichen wird der **like** -Operator flexibler als die Verwendung der Zeichenfolgenvergleichs Operatoren = und!. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *Ausdruck*  NICHT **Wie** *Muster*  [ESCAPE- *EscapeChar* ] 
  
Der **like** -Operator enthält die folgenden Argumente 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *Ausdruck*  <br/> |Ja  <br/> |Ein gültiger Ausdruck.  <br/> |
| *Pattern*  <br/> |Ja  <br/> |Die bestimmte Zeichenfolge, nach der in *Expression* gesucht werden soll. Kann Platzhalterzeichen enthalten. In den Hinweisen finden Sie eine Liste gültiger Platzhalterzeichen.  <br/> |
| *EscapeChar*  <br/> |Nein  <br/> |Ein Zeichen, das vor ein Platzhalterzeichen gestellt wird, um anzugeben, dass der Platzhalter als reguläres Zeichen und nicht als Platzhalter interpretiert werden soll.  *EscapeChar* ist ein Zeichenausdruck, der keinen Standardwert hat und nur einem Zeichen entspricht.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die folgende Tabelle enthält die Platzhalterzeichen, die für die Verwendung im *Pattern* -Argument gültig sind. 
  
|**Platzhalterzeichen**|**Beschreibung**|**Beispiel**|
|:-----|:-----|:-----|
|%  <br/> |Eine beliebige Zeichenfolge mit NULL oder mehr Zeichen.  <br/> | *Wobei der Titel wie "% Computer%"* alle Buchtitel mit dem Wort "Computer" an beliebiger Stelle im Buchtitel findet.  <br/> |
|_ (Unterstrich)  <br/> |Ein beliebiges einzelnes Zeichen.  <br/> | *Wobei AU_FNAME wie "_ean"* alle vier Buchstaben Vornamen findet, die mit EAN (Dean, Sean usw.) enden.  <br/> |
|[]  <br/> |Ein beliebiges einzelnes Zeichen innerhalb des angegebenen Bereich ([a-f]) oder Set ([abcdef]).  <br/> | *Dabei sucht au_lname wie ' [C-P] arsen '* nach Nachnamen, die mit Arsen enden und mit einem einzelnen Zeichen zwischen C und P beginnen, beispielsweise Carsen, Larsen, Karsen usw.  <br/> |
|[^]  <br/> |Ein einzelnes Zeichen, das sich nicht innerhalb des angegebenen Bereich ([^ a-f]) oder Set ([^ abcdef]) befindet.  <br/> | *Wobei au_lname wie ' de [^ l]% '* alle Autorennachnamen beginnend mit de und wobei der folgende Buchstabe nicht l lautet.  <br/> |
   
Wenn Sie Zeichenfolgenvergleiche mit **like**ausführen, sind alle Zeichen in der Musterzeichenfolge signifikant. Hierzu gehören führende oder nachfolgende Leerzeichen. Wenn bei einem Vergleich in einer Abfrage alle Zeilen mit einer Zeichenfolge **wie** "ABC" (ABC gefolgt von einem einzelnen Leerzeichen) zurückgegeben werden sollen, wird keine Zeile zurückgegeben, in der der Wert dieser Spalte ABC (ABC ohne Leerzeichen) ist. Nachstehende Leerzeichen in dem Ausdruck, mit dem das Muster übereinstimmt, werden jedoch ignoriert. Wenn bei einem Vergleich in einer Abfrage alle Zeilen mit der Zeichenfolge **wie** "ABC" (ABC ohne Leerzeichen) zurückgegeben werden sollen, werden alle Zeilen zurückgegeben, die mit ABC beginnen und NULL oder mehr Nachgestellte Leerstellen aufweisen. 
  
Wenn eines der Argumente kein String-Datentyp ist, wird es in einen String-Datentyp konvertiert, falls möglich.
  

