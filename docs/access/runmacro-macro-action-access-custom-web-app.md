---
title: RunMacro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Sie können die RunMacro-Aktion verwenden, um ein Benutzeroberflächen Makro auszuführen.
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307966"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>RunMacro-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **RunMacro** -Aktion verwenden, um ein Benutzeroberflächen Makro auszuführen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **AusführenMakro**-Aktion hat die folgenden Argumente. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
|**Makroname** <br/> |Der Name des auszuführenden Benutzeroberflächen Makros.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Benutzeroberflächen Makro ausführen, das die **RunMacro** -Aktion enthält, und es die **RunMacro** -Aktion erreicht, wird das aufgerufene Benutzeroberflächen Makro von Access ausgeführt. Wenn das aufgerufene Benutzeroberflächen Makro beendet wurde, kehrt Access zum ursprünglichen Benutzeroberflächen Makro zurück und führt die nächste Aktion aus. 
  

