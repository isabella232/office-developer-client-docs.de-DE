---
title: StopMacro-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Sie können die StopMacro-Aktion verwenden, um das aktuell ausgeführte Makro zu beenden.
ms.openlocfilehash: 873937805bb96584dc08708cf2fe4eeadeec8b03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614731"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>StopMacro-Makroaktion (benutzerdefinierte Access-Web-App)

Sie können die **StopMacro-Aktion** verwenden, um das aktuell ausgeführte Makro zu beenden. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **StopMacro-Aktion** hat keine Argumente. 
  
## <a name="remarks"></a>Bemerkungen

In der Regel verwenden Sie diese Aktion, wenn eine Bedingung das Beenden des Makros erforderlich macht. Sie können z. B. ein Benutzeroberflächenmakro erstellen, das eine Ansicht mit den Täglichen Auftragssummen für das in der aktuellen Ansicht eingegebene Datum öffnet. Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement Bestelldatum im Dialogfeld ein gültiges Datum enthält. Andernfalls kann die **MessageBox-Aktion** eine Fehlermeldung anzeigen, und die **StopMacro-Aktion** kann das Benutzeroberflächenmakro beenden. 
  

