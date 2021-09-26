---
title: IS [NOT] NULL (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Bestimmt, ob ein angegebener Ausdruck NULL ist.
ms.localizationpriority: high
ms.openlocfilehash: 47505421c947c7eb76d006bb663866cbbdafbd5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601548"
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
| *NOT*  <br/> |Gibt an, dass das boolesche Ergebnis negiert werden soll. Das Prädikat kehrt seine Rückgabewerte um und gibt TRUE zurück, wenn der Wert nicht NULL ist, und FALSE, wenn der Wert NULL ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der Wert von *expression* NULL ist, gibt IS NULL „TRUE“ zurück; andernfalls wird „FALSE“ zurückgegeben. 
  
Wenn der Wert von expression NULL ist, gibt IS NULL „FALSE“ zurück; andernfalls wird „TRUE“ zurückgegeben.
  

