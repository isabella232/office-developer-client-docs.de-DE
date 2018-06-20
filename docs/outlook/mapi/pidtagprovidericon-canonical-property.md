---
title: Kanonische PidTagProviderIcon-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794838"
---
# <a name="pidtagprovidericon-canonical-property"></a>Kanonische PidTagProviderIcon-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Unicodezeichenfolge, die ein benutzerdefiniertes Symbol oder Symbole für einen MAPI-Anbieter in der Statusleiste von Microsoft Office Outlook im online und offline Zustand anzuzeigende angibt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PROVIDER_ICON PR_PROVIDER_ICON_W  <br/> |
|Bezeichner:  <br/> |0x3417  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften geben Sie die Ressourcendatei, die ein benutzerdefiniertes Symbol enthält, die einen MAPI-Anbieter Status online, darstellt und optional ein anderes benutzerdefiniertes Symbol in den Offlinemodus. Outlook fordert immer diese Eigenschaften im Unicode-Darstellung. 
  
Beispielsweise weist die folgenden Eigenschaftswert Outlook Symbol-ID 1001 aus der mymod32.dll Modul zu laden, und verwenden Sie das Symbol für den Status online: `mymod32.dll,#1001`. Da kein anbieterspezifische Symbol für den Status offline vorhanden ist, wird in diesem Fall das standard-Outlook-offline-Symbol in der Statusleiste angezeigt. 
  
Der Wert der folgenden-Eigenschaft weist Outlook zum Symbol-ID 1001 aus dem Modul mymod32.dll laden und verwenden Sie das Symbol für den Status online und Symbol-ID 1002 auch aus der gleichen Modul für die offline-Status zu verwendende geladen: `mymod32.dll,#1001,#1002`. Kein Outlook-Symbol wird in der Statusleiste verwendet. 
  
Standardmäßig wird der Anbieter keine benutzerdefinierten Symbolen angegeben, durch die Outlook-Standard-Symbole für den Status online und offline-Status dargestellt. Der Anbieter kann optional einen Anzeigenamen ein, in der Statusleiste neben dem Symbol angezeigt werden soll angeben. Weitere Informationen finden Sie unter **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

