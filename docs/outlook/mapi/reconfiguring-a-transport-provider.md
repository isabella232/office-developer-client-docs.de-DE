---
title: Neukonfigurieren eines Transport Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328413"
---
# <a name="reconfiguring-a-transport-provider"></a>Neukonfigurieren eines Transport Anbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mit dem Status-Objekt eines Transportanbieters können Sie einige der Eigenschaften des Anbieters ändern. Der Eigenschaftentyp, der geändert werden kann, hängt von den Eigenschaften ab, die im Eigenschaftenfenster des Anbieters enthalten sind, und davon, wie diese Eigenschaften definiert werden. 
  
 **So konfigurieren Sie einen aktiven Transportanbieter neu**
  
1. Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen. 
    
2. Suchen Sie die Zeile für den Transportanbieter, die neu konfiguriert werden soll, indem Sie eine Eigenschaftseinschränkung erstellen, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des Zielanbieters entspricht. 
    
3. Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um die entsprechende Zeile abzurufen. 
    
4. Überprüfen Sie, ob die STATUS_SETTINGS_DIALOG-und STATUS_VALIDATE_STATE-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Ziel Transportanbieters festgelegt sind. Wenn STATUS_SETTINGS_DIALOG nicht festgelegt ist, wird vom Transportanbieter kein Konfigurationseigenschaften Fenster angezeigt. Wenn STATUS_VALIDATE_STATE nicht festgelegt ist, können Sie die dynamische Neukonfiguration nicht ausführen.
    
5. Wenn STATUS_SETTINGS_DIALOG festgelegt ist, rufen Sie [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) auf, um das Eigenschaftenfenster des Transportanbieters anzuzeigen und dem Benutzer die Möglichkeit zu geben, Änderungen vorzunehmen. 
    
6. Nachdem der Benutzer die Neukonfiguration abgeschlossen hat, rufen Sie [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) auf, wenn STATUS_VALIDATE_STATE festgelegt ist, CONFIG_CHANGED übergeben. 
    

