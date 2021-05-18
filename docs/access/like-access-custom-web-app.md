---
title: LIKE (Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Bestimmt, ob eine bestimmte Zeichenzeichenfolge einem angegebenen Muster entspricht. Ein Muster kann reguläre Zeichen und Platzhalterzeichen enthalten. Beim Musterabgleich müssen reguläre Zeichen genau mit den in der Zeichenzeichenfolge angegebenen Zeichen übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Fragmenten der Zeichenzeichenfolge übereinstimmen. Die Verwendung von Platzhalterzeichen macht den LIKE-Operator flexibler als die Verwendung der Zeichenfolgenvergleichsoperatoren = und != .
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406115"
---
# <a name="like-access-custom-web-app"></a>LIKE (Benutzerdefinierte Access-Web-App)

Bestimmt, ob eine bestimmte Zeichenzeichenfolge einem angegebenen Muster entspricht. Ein Muster kann reguläre Zeichen und Platzhalterzeichen enthalten. Beim Musterabgleich müssen reguläre Zeichen genau mit den in der Zeichenzeichenfolge angegebenen Zeichen übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Fragmenten der Zeichenzeichenfolge übereinstimmen. Die Verwendung von Platzhalterzeichen macht den **LIKE-Operator** flexibler als die Verwendung der Zeichenfolgenvergleichsoperatoren = und != . 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *Ausdruck*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ] 
  
Der **LIKE-Operator** enthält die folgenden Argumente 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *Ausdruck*  <br/> |Ja  <br/> |Ein gültiger Ausdruck.  <br/> |
| *Pattern*  <br/> |Ja  <br/> |Die bestimmte Zeichenfolge von Zeichen, nach der in Expression gesucht *werden soll.* Kann Platzhalterzeichen enthalten. Eine Liste gültiger Platzhalterzeichen finden Sie in den Anmerkungen.  <br/> |
| *EscapeChar*  <br/> |Nein  <br/> |Ein Zeichen, das vor einem Platzhalterzeichen steht, um anzugeben, dass der Platzhalter als reguläres Zeichen und nicht als Platzhalter interpretiert werden soll.  *EscapeChar*  ist ein Zeichenausdruck, der keine Standardeinstellung hat und nur ein Zeichen enthalten muss.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die folgende Tabelle enthält die Platzhalterzeichen, die für die Verwendung im  *Argument Pattern gültig*  sind. 
  
|**Platzhalterzeichen**|**Beschreibung**|**Beispiel**|
|:-----|:-----|:-----|
|%  <br/> |Eine Beliebige Zeichenfolge von null oder mehr Zeichen.  <br/> | *Where title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title.  <br/> |
|_ (Unterstrich)  <br/> |Ein beliebiges einzelnes Zeichen.  <br/> | *Where au_fname LIKE '_ean'*  finds all four-letter first names that end with ean (Dean, Sean, and so on).  <br/> |
|[]  <br/> |Ein beliebiges einzelnes Zeichen innerhalb des angegebenen Bereichs ([a-f]) oder set ([abcdef]).  <br/> | *Where au_lname LIKE '[C-P]arsen'*  finds author last names ending with arsen and starting with any single character between C and P, for example Carsen, Larsen, Karsen, and so weiter.  <br/> |
|[^]  <br/> |Ein einzelnes Zeichen, das sich nicht innerhalb des angegebenen Bereichs ([^a-f]) oder festgelegt ([^abcdef]) befindet.  <br/> | *WHERE au_lname WIE "de[^l]%"*  alle Autorennamen beginnend mit de und wobei der folgende Buchstabe nicht l ist.  <br/> |
   
Wenn Sie Zeichenfolgenvergleiche mithilfe von **LIKE** durchführen, sind alle Zeichen in der Musterzeichenfolge wichtig. Dazu gehören führende oder nachgestellte Leerzeichen. Wenn bei einem Vergleich in einer Abfrage alle Zeilen mit einer Zeichenfolge **wie** "abc" (abc gefolgt von einem einzelnen Leerzeichen) zurückgegeben werden sollen, wird keine Zeile zurückgegeben, in der der Wert dieser Spalte abc (abc ohne Leerzeichen) ist. Nachgestellte Leerzeichen im Ausdruck, dem das Muster entspricht, werden jedoch ignoriert. Wenn bei einem Vergleich in einer Abfrage alle Zeilen mit der Zeichenfolge **LIKE** "abc" (abc ohne Leerzeichen) zurückgegeben werden sollen, werden alle Zeilen zurückgegeben, die mit abc beginnen und null oder mehr nachgestellte Leerzeichen enthalten. 
  
Wenn eines der Argumente keinen Zeichenfolgendatentyp hat, wird es in einen Zeichenfolgendatentyp konvertiert, sofern dies möglich ist.
  

