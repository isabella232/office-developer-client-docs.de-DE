---
title: ZWISCHEN (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Gibt einen Bereich zu testen.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790203"
---
# <a name="between-access-custom-web-app"></a>ZWISCHEN (Access benutzerdefinierte Web app)

Gibt einen Bereich zu testen.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *test_expression*  [NOT] **BETWEEN** *begin_expression* **Und** *end_expression* 
  
Der Operator **zwischen** enthält die folgenden Argumente. 
  
|**Argument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Ja  <br/> |Der Ausdruck, der im Bereich von *Begin_expression* und *End_expression* definierten testen. Muss denselben Datentyp aufweisen wie *Begin_expression* und *End_expression* .  <br/> |
| *NOT*  <br/> |Nein  <br/> |Gibt an, dass das Ergebnis des Prädikats negiert werden soll.  <br/> |
| *begin_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Muss denselben Datentyp aufweisen wie *Test_expression* und *End_expression* .  <br/> |
| *end_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Denselben Datentyp aufweisen wie *Test_expression* und *Begin_expression* muss sein.  <br/> |
| *AND*  <br/> |Ja  <br/> |Gibt an, dass *Test_expression* innerhalb des Bereichs von *Begin_expression* und *End_expression* angegeben werden soll.  <br/> |
   
## <a name="result-type"></a>Ergebnistyp

 **Boolean**
  
## <a name="remarks"></a>Bemerkungen

 **BETWEEN** gibt **TRUE** zurück, wenn der Wert von *Test_expression* größer als oder gleich dem Wert von *Begin_expression* ist kleiner oder gleich dem Wert von *End_expression* . 
  
 **Nicht zwischen** zurückgegeben **TRUE** , wenn der Wert von *Test_expression* kleiner als der Wert von *Begin_expression* oder größer als der Wert von *End_expression* ist. 
  
Verwenden Sie zum Angeben eines Bereichs, der größer als (\>) und kleiner als Operatoren (\<).
  

