---
title: AusführenDatenmakro-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Die AusführenDatenmakro-Aktion können Sie eine eigenständige Datenmakro ausführen.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790349"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>AusführenDatenmakro-Makroaktion (Access benutzerdefinierte Web app)

Die **AusführenDatenmakro** -Aktion können Sie eine eigenständige Datenmakro ausführen. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **AusführenDatenmakro** -Aktion kann mit dem folgenden Argument verwendet werden. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
| _Makroname_ <br/> |Der Name des Datenmakros, das ausgeführt werden soll.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert. Wenn das Datenmakro Parameter erfordert, erscheinen Textfelder, in dem Sie die Argumente eingeben können.
  
Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus. 
  

