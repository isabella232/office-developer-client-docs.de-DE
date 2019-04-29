---
title: Ausführendatenmakro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Sie können die Ausführendatenmakro-Aktion verwenden, um ein eigenständiges datenmakro auszuführen.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439345"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>Ausführendatenmakro-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **ausführendatenmakro** -Aktion verwenden, um ein eigenständiges datenmakro auszuführen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **AusführenDatenmakro**-Aktion kann mit dem folgenden Argument verwendet werden. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
| _Makroname_ <br/> |Der Name des Datenmakros, das ausgeführt werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert. Wenn das datenmakro Parameter erfordert, werden Textfelder angezeigt, in denen Sie die Argumente eingeben können.
  
Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus. 
  

