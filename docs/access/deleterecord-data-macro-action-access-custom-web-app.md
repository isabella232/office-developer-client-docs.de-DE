---
title: DeleteRecord Data-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Mit der DatensatzLöschen -Aktion können Sie einen Datensatz löschen.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282115"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>DeleteRecord Data-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **DeleteRecord** -Aktion hat die folgenden Argumente. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|**Datensatzalias** <br/> |Eine Zeichenfolge, mit der der zu löschende Datensatz gekennzeichnet wird. Wenn das Argument *Alias* nicht angegeben wird, wird der aktuelle Datensatz gelöscht.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Verwenden Sie beispielsweise die folgende Syntax, um auf den zuletzt erstellten Datensatz zu verweisen: 
  
`[LastCreateRecordIdentity]`


