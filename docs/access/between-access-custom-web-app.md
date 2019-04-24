---
title: BeTWEEN (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Gibt einen zu testenden Test an.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280743"
---
# <a name="between-access-custom-web-app"></a>BeTWEEN (Access Custom Web App)

Gibt einen zu testenden Test an.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *test_expression*  NICHT **Zwischen** *begin_expression* **Und** *end_expression* 
  
Der **** Operator BETWEEN enthält die folgenden Argumente. 
  
|**Argument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Ja  <br/> |Der Ausdruck, der in dem durch *begin_expression* und *end_expression* definierten Range getestet werden soll. Muss derselbe Datentyp wie *begin_expression* und *end_expression* sein.  <br/> |
| *NOT*  <br/> |Nein  <br/> |Gibt an, dass das Ergebnis des Prädikats negiert werden soll.  <br/> |
| *begin_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Muss derselbe Datentyp wie *test_expression* und *end_expression* sein.  <br/> |
| *end_expression*  <br/> |Ja  <br/> |Ein gültiger Ausdruck. Muss derselbe Datentyp wie *test_expression* und *begin_expression* sein.  <br/> |
| *AND*  <br/> |Ja  <br/> |Gibt an, dass *test_expression* innerhalb des von *begin_expression* und *end_expression* angegebenen Bereich liegen sollte.  <br/> |
   
## <a name="result-type"></a>Ergebnistyp

 **Boolean**
  
## <a name="remarks"></a>Hinweise

 **Zwischen** gibt **true** zurück, wenn der Wert von *test_expression* größer als oder gleich dem Wert von *begin_expression* und kleiner als oder gleich dem Wert von *end_expression* ist. 
  
 **Nicht zwischen** gibt **true** zurück, wenn der Wert von *test_expression* kleiner als der Wert von *begin_expression* oder größer als der Wert von *end_expression* ist. 
  
Um einen exklusiven Range anzugeben, verwenden Sie den Wert größer\>als () und kleiner als\<Operatoren ().
  

