---
title: LöschenDatensatz-Makroaktion (benutzerdefinierte Access-Web-App)
manager: lindalu
ms.date: 09/05/2021
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
ms.openlocfilehash: 01d0cdeecd7c1401c274822736a3cd40a865db52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586432"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>LöschenDatensatz-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **DeleteRecord-Aktion** hat die folgenden Argumente. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|**Datensatzalias** <br/> |Eine Zeichenfolge, mit der der zu löschende Datensatz gekennzeichnet wird. Wenn das  *Alias-Argument*  nicht angegeben ist, wird der aktuelle Datensatz gelöscht.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Verwenden Sie beispielsweise die folgende Syntax, um auf den zuletzt erstellten Datensatz zu verweisen: 
  
`[LastCreateRecordIdentity]`
