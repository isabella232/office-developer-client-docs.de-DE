---
title: IS [NOT] NULL (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Bestimmt, ob ein angegebener Ausdruck NULL ist.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311137"
---
# <a name="is-not-null-access-custom-web-app"></a>IS [NOT] NULL (benutzerdefinierte Access-Web-App)

Bestimmt, ob ein angegebener Ausdruck NULL ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *expression* **IS** [  *NOT*  ] **NULL**
  
Das Prädikat **IS [NOT] NULL** enthält die folgenden Argumente. 
  
|||
|:-----|:-----|
| *expression*  <br/> |Jeder gültige Ausdruck.  <br/> |
| *NOT*  <br/> |Gibt an, dass das boolesche Ergebnis negiert werden soll. Das Prädikat kehrt die Rückgabewerte um, sodass TRUE zurückgegeben wird, wenn der Wert nicht NULL ist, und FALSE, wenn der Wert NULL ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der Wert von *expression* NULL ist, gibt IS NULL „TRUE“ zurück; andernfalls wird „FALSE“ zurückgegeben. 
  
Wenn der Wert von expression NULL ist, gibt IS NULL „FALSE“ zurück; andernfalls wird „TRUE“ zurückgegeben.
  

