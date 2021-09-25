---
title: BETWEEN (Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Gibt einen zu testden Bereich an.
ms.openlocfilehash: 85fea11c3cf658ef6b5f821cd54304c64aa06743
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562881"
---
# <a name="between-access-custom-web-app"></a>BETWEEN (Benutzerdefinierte Access-Web-App)

Gibt einen zu testden Bereich an.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *test_expression*  [ NICHT ] **ZWISCHEN** *begin_expression* **UND** *end_expression* 
  
Der **Between-Operator** enthält die folgenden Argumente. 
  
|**Argument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Ja  <br/> |Der Ausdruck, auf den in dem durch begin_expression und  *end_expression*  definierten Bereich  *getestet werden*  soll. Muss der gleiche Datentyp wie  *begin_expression*  und  *end_expression*  sein.  <br/> |
| *NOT*  <br/> |Nein  <br/> |Gibt an, dass das Ergebnis des Prädikats negiert wird.  <br/> |
| *Begin_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Muss der gleiche Datentyp wie  *test_expression*  und  *end_expression*  sein.  <br/> |
| *End_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Muss der gleiche Datentyp wie  *test_expression*  und  *begin_expression*  sein.  <br/> |
| *AND*  <br/> |Ja  <br/> |Gibt  *an, test_expression*  innerhalb des bereichs liegen soll, der durch  *begin_expression*  und  *end_expression*  angegeben wird.  <br/> |
   
## <a name="result-type"></a>Ergebnistyp

 **Boolean**
  
## <a name="remarks"></a>Bemerkungen

 **BETWEEN** gibt **TRUE** zurück, wenn der Wert von  *test_expression*  größer oder gleich dem Wert von  *begin_expression*  und kleiner oder gleich dem Wert von  *end_expression*  ist. 
  
 **NOT BETWEEN** gibt **TRUE** zurück, wenn der Wert von  *test_expression*  kleiner als der Wert von  *begin_expression*  oder größer als der Wert von  *end_expression*  ist. 
  
Um einen exklusiven Bereich anzugeben, verwenden Sie die Operatoren größer als ( \> ) und kleiner als Operatoren ( \< ).
  

