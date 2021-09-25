---
title: AusführenMakro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Mit der Aktion "AusführenMakro" können Sie ein Benutzeroberflächenmakro ausführen.
ms.openlocfilehash: e91fba9461002c1cb9cc029448b72bff5f77c365
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552339"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>AusführenMakro-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **Aktion "AusführenMakro"** können Sie ein Benutzeroberflächenmakro ausführen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **AusführenMakro**-Aktion hat die folgenden Argumente. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
|**Makroname** <br/> |Der Name des auszuführenden Benutzeroberflächenmakros.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie ein Benutzeroberflächenmakro ausführen, das die **RunMacro-Aktion** enthält, und es die **RunMacro-Aktion** erreicht, führt Access das aufgerufene Benutzeroberflächenmakro aus. Wenn das aufgerufene Benutzeroberflächenmakro abgeschlossen ist, kehrt Access zum ursprünglichen Benutzeroberflächenmakro zurück und führt die nächste Aktion aus. 
  

