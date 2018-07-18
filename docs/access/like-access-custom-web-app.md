---
title: WIE (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Bestimmt, ob eine bestimmte Zeichenfolge mit einem angegebenen Muster entspricht. Ein Muster kann normale Zeichen und Platzhalterzeichen enthalten. Bei einem Mustervergleich müssen normale Zeichen genau die angegebenen Zeichen in der Zeichenfolge übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Teilen der Zeichenfolge übereinstimmen. Verwenden von Platzhalterzeichen wird den LIKE-Operator flexibler als die Verwendung der = und! = Zeichenfolge Vergleichsoperatoren.
ms.openlocfilehash: d3224647c621b05a08bdc863939d0cccae214463
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790241"
---
# <a name="like-access-custom-web-app"></a>WIE (Access benutzerdefinierte Web app)

Bestimmt, ob eine bestimmte Zeichenfolge mit einem angegebenen Muster entspricht. Ein Muster kann normale Zeichen und Platzhalterzeichen enthalten. Bei einem Mustervergleich müssen normale Zeichen genau die angegebenen Zeichen in der Zeichenfolge übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Teilen der Zeichenfolge übereinstimmen. Verwenden von Platzhalterzeichen wird den Operator **LIKE** flexibler als die Verwendung der = und! = Zeichenfolge Vergleichsoperatoren. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *Ausdruck*  [NOT] **Wie** *Muster*  [ESCAPE *EscapeChar* ] 
  
Der Operator **LIKE** enthält die folgenden Argumente. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *Expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck.  <br/> |
| *Pattern*  <br/> |Ja  <br/> |Die bestimmte Zeichenfolge in *Ausdruck* suchen. Kann Platzhalterzeichen enthalten. Finden Sie in den Hinweisen für eine Liste der gültigen Platzhalterzeichen.  <br/> |
| *EscapeChar*  <br/> |Nein  <br/> |Ein Zeichen, das vor einem Platzhalterzeichen an, dass den Platzhalter versetzt wurde, sollte als normales Zeichen und nicht als Platzhalter interpretiert werden.  *EscapeChar* ist ein Zeichenausdruck, der hat keinen Standardwert und muss nur ein Zeichen ergeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die folgende Tabelle enthält die Platzhalterzeichen, die für die Verwendung im Argument *Muster* gültig sind. 
  
|**Platzhalterzeichen**|**Description**|**Beispiel**|
|:-----|:-----|:-----|
|%  <br/> |Eine Zeichenfolge mit NULL oder mehr Zeichen.  <br/> | Sucht nach alle Buchtitel mit dem Wort "Computer" *, in dem Titel LIKE '% Computer %'* an einer beliebigen Stelle in der Buchtitel.  <br/> |
|_ (Unterstrich)  <br/> |Ein beliebiges einzelnes Zeichen.  <br/> | *WHERE Au_fname LIKE '_ean'* sucht nach allen Vornamen mit vier Buchstaben, die mit Ean (Dominik, Sean usw.) enden.  <br/> |
|[]  <br/> |Beliebiges einzelnes Zeichen innerhalb des angegebenen Bereichs ([a-f]) oder Menge ([Abcdef]).  <br/> | *WHERE Au_lname LIKE '[C-P] Arsen'* sucht Autorennamen Arsen enden und beginnend mit einem einzelnen Zeichen zwischen C und P beginnen, beispielsweise Carsen, Larsen, Karsen, und so weiter.  <br/> |
|[^]  <br/> |Ein beliebiges einzelnes Zeichen nicht innerhalb des angegebenen Bereichs ([^ a-f]) oder festgelegt ([^ Abcdef]).  <br/> | *WHERE Au_lname LIKE ' de [^ l] %'* alle Autorennamen, die beginnend mit de und deren dritter Buchstabe nicht l ist.  <br/> |
   
Wenn Sie mithilfe von **wie**Zeichenfolgenvergleiche ausführen, sind alle Zeichen in der Musterzeichenfolge beträchtlich. Dazu gehören Leerzeichen beginnen oder enden. Wenn in einer Abfrage wird, um alle Zeilen mit **LIKE** 'Abc' (Abc, gefolgt von einem einzelnen Leerzeichen) zurückgeben, wird eine Zeile, in der der Wert dieser Spalte Abc (Abc ohne Leerzeichen) ist, nicht zurückgegeben. Nachfolgende Leerzeichen in dem Ausdruck, den mit das Muster verglichen wird, werden jedoch ignoriert. Wenn in einer Abfrage wird, um alle Zeilen mit **LIKE** 'Abc' (Abc ohne Leerzeichen) zurückgeben, werden alle Zeilen, die mit Abc anfangen und NULL oder mehr nachfolgende Leerzeichen zurückgegeben. 
  
Wenn eines der Argumente nicht vom Datentyp String ist, wird es in einen String-Datentyp konvertiert, wenn es möglich ist.
  

