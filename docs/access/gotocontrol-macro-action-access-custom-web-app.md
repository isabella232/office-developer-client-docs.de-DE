---
title: GeheZuSteuerelement-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Mit der GeheZuSteuerelement-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht verschieben.
ms.openlocfilehash: 5323f1daff2e8ae76c9aa24e6a40b907b6396030
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572473"
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
  

