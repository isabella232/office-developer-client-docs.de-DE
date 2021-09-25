---
title: SetProperty-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Mit der Aktion "SetProperty" können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festlegen.
ms.openlocfilehash: 1f72d038d522b9ed6e1b1c6d27dd948d8ee7352a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601492"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>SetProperty-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **Aktion "SetProperty"** können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festlegen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **Aktion "SetProperty"** enthält die In der folgenden Tabelle aufgeführten Argumente. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
| _Steuerelementname_ <br/> |Geben Sie den Namen des Felds oder Steuerelements ein, für das Sie den Eigenschaftswert festlegen möchten. Lassen Sie dieses Argument leer, um die Eigenschaft für die Ansicht festzulegen.  <br/> |
| _Eigenschaft_ <br/> |Wählen Sie die Eigenschaft aus, die Sie festlegen möchten. Der Abschnitt **Hinweise** in diesem Artikel enthält eine Auflistung der Eigenschaften, die mithilfe dieser Aktion festgelegt werden können.<br/> |
| _Wert_ <br/> |Geben Sie den Wert ein, auf den die Eigenschaft festgelegt werden soll. Verwenden Sie für Eigenschaften, deren Werte entweder "Ja" oder "Nein" lauten, **"-1"** für "Ja" und **"0"** für "Nein".  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Mit der **Aktion "SetProperty"** können Sie die folgenden Eigenschaften eines Steuerelements festlegen: 
  
- Beschriftung
    
- Aktiviert
    
- ForeColor
    
- Wert
    
- Visible
    
Wenn Sie einen ungültigen Wert für das Argument ** *Wert* ** eingeben, tritt kein Fehler auf. Allerdings kann es passieren, dass Access die Eigenschaft in einen anderen Wert ändert. Dies hängt davon ab, wie das Argument interpretiert wird. 
  

