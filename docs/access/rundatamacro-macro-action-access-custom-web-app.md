---
title: RunDataMacro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Mit der RunDataMacro-Aktion können Sie ein eigenständiges Datenmakro ausführen.
ms.openlocfilehash: 4505bf5eadda4cf0c12af73b050826b6493be139
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580601"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>RunDataMacro-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **RunDataMacro-Aktion** können Sie ein eigenständiges Datenmakro ausführen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **AusführenDatenmakro**-Aktion kann mit dem folgenden Argument verwendet werden. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
| _Makroname_ <br/> |Der Name des Datenmakros, das ausgeführt werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert. Wenn für das Datenmakro Parameter erforderlich sind, werden Textfelder angezeigt, in die Sie die Argumente eingeben können.
  
Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus. 
  

