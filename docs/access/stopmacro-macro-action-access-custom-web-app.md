---
title: StoppMakro-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Die StoppMakro-Aktion können Sie das derzeit ausgeführte Makro anzuhalten.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790360"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>StoppMakro-Makroaktion (Access benutzerdefinierte Web app)

Die **StoppMakro** -Aktion können Sie das derzeit ausgeführte Makro anzuhalten. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **StoppMakro** -Aktion verfügt nicht über keine Argumente. 
  
## <a name="remarks"></a>Hinweise

Normalerweise verwenden Sie diese Aktion, wenn eine Bedingung das Makro anzuhalten vornimmt. Beispielsweise können Sie ein Benutzer Benutzeroberfläche (UI)-Makro erstellen, das eine Ansicht mit der täglichen Summen Reihenfolge für das Datum in der aktuellen Ansicht geöffnet wird. Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement Bestelldatum im Dialogfeld ein gültiges Datum enthält. Wenn dies nicht der Fall, die **Abfrageergebnis** -Aktion kann eine Fehlermeldung angezeigt, und die **StoppMakro** -Aktion kann das UI-Makro beenden. 
  

