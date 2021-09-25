---
title: LIKE (Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Bestimmt, ob eine bestimmte Zeichenzeichenfolge mit einem angegebenen Muster übereinstimmt. Ein Muster kann reguläre Zeichen und Platzhalterzeichen enthalten. Beim Musterabgleich müssen reguläre Zeichen genau mit den in der Zeichenzeichenfolge angegebenen Zeichen übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Fragmenten der Zeichenzeichenfolge abgeglichen werden. Die Verwendung von Platzhalterzeichen macht den LIKE-Operator flexibler als die Zeichenfolgenvergleichsoperatoren = und !=.
ms.openlocfilehash: 0ad520b8bf9acd10134f73c016c5ddc984e9e51a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568229"
---
# <a name="like-access-custom-web-app"></a>LIKE (Benutzerdefinierte Access-Web-App)

Bestimmt, ob eine bestimmte Zeichenzeichenfolge mit einem angegebenen Muster übereinstimmt. Ein Muster kann reguläre Zeichen und Platzhalterzeichen enthalten. Beim Musterabgleich müssen reguläre Zeichen genau mit den in der Zeichenzeichenfolge angegebenen Zeichen übereinstimmen. Platzhalterzeichen können jedoch mit beliebigen Fragmenten der Zeichenzeichenfolge abgeglichen werden. Die Verwendung von Platzhalterzeichen macht den **LIKE-Operator** flexibler als die Zeichenfolgenvergleichsoperatoren = und !=. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *Ausdruck*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ] 
  
Der **LIKE-Operator** enthält die folgenden Argumente 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *Ausdruck*  <br/> |Ja  <br/> |Ein gültiger Ausdruck.  <br/> |
| *Pattern*  <br/> |Ja  <br/> |Die spezifische Zeichenfolge von Zeichen, nach denen in  *Ausdruck*  gesucht werden soll. Kann Platzhalterzeichen enthalten. Eine Liste gültiger Platzhalterzeichen finden Sie in den Hinweisen.  <br/> |
| *EscapeChar*  <br/> |Nein  <br/> |Ein Zeichen, das vor einem Platzhalterzeichen platziert wird, um anzugeben, dass der Platzhalter als reguläres Zeichen und nicht als Platzhalter interpretiert werden soll.  *EscapeChar*  ist ein Zeichenausdruck, der keinen Standardwert aufweist und nur zu einem Zeichen ausgewertet werden muss.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die folgende Tabelle enthält die Platzhalterzeichen, die für die Verwendung im  *Pattern-Argument*  gültig sind. 
  
|**Platzhalterzeichen**|**Beschreibung**|**Beispiel**|
|:-----|:-----|:-----|
|%  <br/> |Eine beliebige Zeichenfolge mit null oder mehr Zeichen.  <br/> | *Where title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title.  <br/> |
|_ (Unterstrich)  <br/> |Ein beliebiges einzelnes Zeichen.  <br/> | *WHERE au_fname LIKE "_ean"*  findet alle Vier-Buchstaben-Vornamen, die mit "Ean" enden (Aufzählung, Sean usw.).  <br/> |
|[]  <br/> |Jedes einzelne Zeichen innerhalb des angegebenen Bereichs ([a-f]) oder festgelegt ([abcdef]).  <br/> | *WHERE au_lname LIKE '[C-P]doppelklicken'*  sucht Nachnamen des Autors, die mit"-Nachnamen enden und mit einem beliebigen einzelnen Zeichen zwischen C und P beginnen, z. B. "Carsen", "Doppelklicken", "Karsen" usw.  <br/> |
|[^]  <br/> |Ein einzelnes Zeichen, das nicht innerhalb des angegebenen Bereichs ([^a-f]) oder festgelegt ([^abcdef]) liegt.  <br/> | *WHERE au_lname LIKE 'de[^l]%'*  alle Nachnamen des Autors beginnend mit de und wobei der folgende Buchstabe nicht l ist.  <br/> |
   
Wenn Sie Zeichenfolgenvergleiche **mit** like durchführen, sind alle Zeichen in der Musterzeichenfolge von Bedeutung. Dazu gehören führende oder nachstehende Leerzeichen. Wenn bei einem Vergleich in einer Abfrage alle Zeilen mit einer Zeichenfolge **WIE** "abc" (abc gefolgt von einem einzelnen Leerzeichen) zurückgegeben werden sollen, wird keine Zeile zurückgegeben, in der der Wert dieser Spalte "abc" (abc ohne Leerzeichen) ist. Nachfolgende Leerzeichen in dem Ausdruck, dem das Muster zugeordnet ist, werden jedoch ignoriert. Wenn ein Vergleich in einer Abfrage darin besteht, alle Zeilen mit der Zeichenfolge **LIKE** 'abc' (abc ohne Leerzeichen) zurückzugeben, werden alle Zeilen zurückgegeben, die mit abc beginnen und null oder mehr leere Zeilen enthalten. 
  
Wenn eines der Argumente keinen Zeichenfolgendatentyp aufweist, wird es in einen Zeichenfolgendatentyp konvertiert, sofern dies möglich ist.
  

