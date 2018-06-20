---
title: '[NOT] ist NULL (Access benutzerdefinierte Web app)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Bestimmt, ob ein bestimmter Ausdruck gleich NULL ist.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790206"
---
# <a name="is-not-null-access-custom-web-app"></a>[NOT] ist NULL (Access benutzerdefinierte Web app)

Bestimmt, ob ein bestimmter Ausdruck gleich NULL ist.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *Ausdruck* **IS** [ *Nicht* ] **NULL**
  
Die **IS [NOT] NULL** Prädikat enthält die folgenden Argumente. 
  
|||
|:-----|:-----|
| *expression*  <br/> |Ein beliebiger gültiger Ausdruck.  <br/> |
| *NOT*  <br/> |Gibt an, dass das boolesche Ergebnis negiert werden soll. Das Prädikat kehrt die Rückgabewerte, gibt TRUE zurück, wenn der Wert nicht NULL ist, und FALSE, wenn der Wert NULL ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der Wert des *Ausdrucks* NULL ist, ISTNULL wird TRUE zurückgegeben. Andernfalls wird FALSE zurückgegeben. 
  
Wenn der Wert des Ausdrucks NULL ist, gibt IS NOT NULL FALSE zurück. Andernfalls wird TRUE zurückgegeben.
  

