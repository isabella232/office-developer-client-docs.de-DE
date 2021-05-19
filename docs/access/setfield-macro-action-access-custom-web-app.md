---
title: SetField-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: Mit der FestlegenFeld -Aktion können Sie einem Feld einen Wert zuweisen.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432926"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>SetField-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Die **FestlegenFeld**-Aktion ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Setting

Die **FestlegenFeld**-Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Eine Zeichenfolge, die das Feld bezeichnet.  <br/> |
|**Wert** <br/> |Ein Ausdruck, der den Wert angibt, der dem Feld zugewiesen werden soll.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **SetField-Aktion** kann nicht außerhalb eines **[CreateRecord-](createrecord-data-block-access-custom-web-app.md)** oder **[EditRecord-Datenblocks](editrecord-data-block-access-custom-web-app.md)** verwendet werden. 
  

