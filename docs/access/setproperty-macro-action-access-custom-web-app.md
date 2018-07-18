---
title: FestlegenEigenschaft-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Die FestlegenEigenschaft-Aktion können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festgelegt.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790352"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>FestlegenEigenschaft-Makroaktion (Access benutzerdefinierte Web app)

Die **FestlegenEigenschaft** -Aktion können Sie eine Eigenschaft für ein Steuerelement in einer Ansicht festgelegt. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **FestlegenEigenschaft** -Aktion hat die Argumente in der folgenden Tabelle aufgeführt. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
| _Steuerelementname_ <br/> |Geben Sie den Namen des Felds oder der Steuerung für den Wert der Eigenschaft festgelegt werden soll. Lassen Sie dieses Argument leer, um die-Eigenschaft für die Ansicht festgelegt.  <br/> |
| _Eigenschaft_ <br/> |Wählen Sie die Eigenschaft aus, die Sie festlegen möchten. Der Abschnitt **Hinweise** in diesem Artikel enthält eine Auflistung der Eigenschaften, die mithilfe dieser Aktion festgelegt werden können.<br/> |
| _Wert_ <br/> |Geben Sie den Wert ein, auf den diese Eigenschaft festgelegt werden soll. Verwenden Sie bei Eigenschaften, deren Werte entweder Ja oder Nein lauten, -1 für Ja und 0 für Nein.<br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **FestlegenEigenschaft** -Aktion können Sie die folgenden Eigenschaften eines Steuerelements festlegen: 
  
- Caption
    
- Aktiviert
    
- ForeColor
    
- Wert
    
- Visible
    
Wenn Sie einen ungültigen Wert für das Argument ** *Wert* ** eingeben, tritt kein Fehler auf. Allerdings kann es passieren, dass Access die Eigenschaft in einen anderen Wert ändert. Dies hängt davon ab, wie das Argument interpretiert wird. 
  

