---
title: BETWEEN (Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Gibt einen zu testden Bereich an.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429299"
---
# <a name="between-access-custom-web-app"></a>BETWEEN (Benutzerdefinierte Access-Web-App)

Gibt einen zu testden Bereich an.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression* 
  
Der **Between-Operator** enthält die folgenden Argumente. 
  
|**Argument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Ja  <br/> |Der Ausdruck, nach dem in  dem von begin_expression und end_expression *definierten Bereich end_expression.* Muss der gleiche Datentyp sein wie begin_expression  *und*  *end_expression*  .  <br/> |
| *NOT*  <br/> |Nein  <br/> |Gibt an, dass das Ergebnis des Prädikats negiert wird.  <br/> |
| *begin_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Muss der gleiche Datentyp sein wie test_expression  *und*  *end_expression*  .  <br/> |
| *end_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Muss der gleiche Datentyp sein wie test_expression  *und*  *begin_expression*  .  <br/> |
| *UND*  <br/> |Ja  <br/> |Gibt *an test_expression* innerhalb des bereichs liegen soll, der durch begin_expression *und* *end_expression.*  <br/> |
   
## <a name="result-type"></a>Ergebnistyp

 **Boolean**
  
## <a name="remarks"></a>Bemerkungen

 **BETWEEN** gibt **TRUE** zurück, wenn der Wert von  *test_expression*  größer oder gleich dem Wert von  *begin_expression*  und kleiner als oder gleich dem Wert von  *end_expression*  ist. 
  
 **NOT BETWEEN** gibt **TRUE zurück,** wenn der Wert von  *test_expression*  kleiner als der Wert von  *begin_expression*  oder größer als der Wert von  *end_expression*  . 
  
Verwenden Sie zum Angeben eines exklusiven Bereichs den Wert größer als ( \> ) und kleiner als Operatoren ( \< ).
  

