---
title: GeheZuSteuerelement-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Mit der GeheZuSteuerelement-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht verschieben.
ms.openlocfilehash: 2368933a6277615554a565d3bdd973f7d1f366f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302576"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a>GeheZuSteuerelement-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **GeheZuSteuerelement**-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht verschieben. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **GeheZuSteuerelement**-Aktion hat die folgenden Argumente. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
|**Steuerelementname** <br/> |Der Name des Felds oder Steuerelements, das den Fokus erhalten soll. Dies ist ein erforderliches Argument.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diese Aktion verwenden, wenn ein bestimmtes Feld oder Steuerelement den Fokus haben soll. Sie können die Aktion auch zum Navigieren in einem Formular basierend auf bestimmten Bedingungen verwenden. Wenn der Benutzer z. B. im Steuerelement „Verheiratet“ auf einem Versicherungsformular „Nein“ angibt, kann der Fokus automatisch das Steuerelement „Name des Partners/der Partnerin“ überspringen und zum nächsten Steuerelement wechseln.
  

