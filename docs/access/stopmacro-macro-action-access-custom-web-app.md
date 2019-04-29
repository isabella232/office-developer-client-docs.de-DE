---
title: Stopmakro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Sie können die Stopmakro-Aktion verwenden, um das derzeit ausgeführte Makro zu beenden.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429495"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>Stopmakro-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **stopmakro** -Aktion verwenden, um das derzeit ausgeführte Makro zu beenden. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **stopmakro** -Aktion hat keine Argumente. 
  
## <a name="remarks"></a>Bemerkungen

Diese Aktion wird in der Regel verwendet, wenn eine Bedingung das Beenden des Makros erforderlich macht. Sie können beispielsweise ein Benutzeroberflächen Makro erstellen, das eine Ansicht öffnet, in der die Gesamtsummen für das in der aktuellen Ansicht eingegebene Datum angezeigt werden. Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement Order Date im Dialogfeld ein gültiges Datum enthält. Wenn dies nicht der Fall ist, kann die **MessageBox** -Aktion eine Fehlermeldung anzeigen, und die **stopmakro** -Aktion kann das Benutzeroberflächen Makro beenden. 
  

