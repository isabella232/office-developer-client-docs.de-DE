---
title: GeheZuSteuerelement-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Mit der GeheZuSteuerelement-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht verschieben.
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790191"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a>GeheZuSteuerelement-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **GeheZuSteuerelement**-Aktion können Sie den Fokus auf das angegebene Steuerelement im aktuellen Datensatz der geöffneten Ansicht verschieben. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-DE/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **GeheZuSteuerelement**-Aktion hat die folgenden Argumente. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
|**Steuerelementname** <br/> |Der Name des Felds oder Steuerelements, das den Fokus erhalten soll. Dies ist ein erforderliches Argument.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diese Aktion verwenden, wenn ein bestimmtes Feld oder Steuerelement den Fokus haben soll. Sie können die Aktion auch zum Navigieren in einem Formular basierend auf bestimmten Bedingungen verwenden. Wenn der Benutzer z. B. im Steuerelement „Verheiratet“ auf einem Versicherungsformular „Nein“ angibt, kann der Fokus automatisch das Steuerelement „Name des Partners/der Partnerin“ überspringen und zum nächsten Steuerelement wechseln.
  

