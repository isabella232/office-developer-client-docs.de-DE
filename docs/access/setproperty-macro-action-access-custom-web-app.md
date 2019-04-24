---
title: SetProperty-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Mit der SetProperty-Aktion können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festlegen.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307889"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>SetProperty-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der SetProperty **** -Aktion können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festlegen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **SetProperty-** Aktion hat die in der folgenden Tabelle aufgeführten Argumente. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
| _Steuerelementname_ <br/> |Geben Sie den Namen des Felds oder Steuerelements ein, für das Sie den Eigenschaftswert festlegen möchten. Lassen Sie dieses Argument leer, um die Eigenschaft für die Ansicht festzulegen.  <br/> |
| _Eigenschaft_ <br/> |Wählen Sie die Eigenschaft aus, die Sie festlegen möchten. Der Abschnitt **Hinweise** in diesem Artikel enthält eine Auflistung der Eigenschaften, die mithilfe dieser Aktion festgelegt werden können.<br/> |
| _Wert_ <br/> |Geben Sie den Wert ein, auf den die Eigenschaft festgelegt werden soll. Für Eigenschaften, deren Werte entweder "Ja" oder "Nein" sind, verwenden Sie **-1** für Yes und **0** für Nein.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mit der SetProperty **-** Aktion können Sie die folgenden Eigenschaften eines Steuerelements festlegen: 
  
- Beschriftung
    
- Aktiviert
    
- ForeColor
    
- Wert
    
- Visible
    
Wenn Sie einen ungültigen Wert für das Argument ** *Wert* ** eingeben, tritt kein Fehler auf. Allerdings kann es passieren, dass Access die Eigenschaft in einen anderen Wert ändert. Dies hängt davon ab, wie das Argument interpretiert wird. 
  

