---
title: PidTagProviderIcon (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425638"
---
# <a name="pidtagprovidericon-canonical-property"></a>PidTagProviderIcon (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicode-Zeichenfolge, die ein benutzerdefiniertes Symbol oder ein benutzerdefiniertes Symbol angibt, das für einen MAPI-Anbieter in der Microsoft Office Outlook Statusleiste im Online- und Offlinestatus angezeigt werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Kennung:  <br/> |0x3417  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften geben die Ressourcendatei an, die ein benutzerdefiniertes Symbol enthält, das einen MAPI-Anbieter in einem Onlinestatus darstellt, und optional ein weiteres benutzerdefiniertes Symbol im Offlinestatus. Outlook fordert diese Eigenschaften immer in der Unicode-Darstellung an. 
  
Der folgende Eigenschaftswert z. B. anweisen Outlook Symbol-ID 1001 aus dem Modul mymod32.dll zu laden und dieses Symbol für den Onlinestatus zu verwenden: `mymod32.dll,#1001` . Da es kein anbieterspezifisches Symbol für den Offlinestatus gibt, wird in diesem Fall das standard-Outlook-Offlinesymbol in der Statusleiste verwendet. 
  
Der folgende Eigenschaftswert wies Outlook an, die Symbol-ID 1001 aus dem Modul mymod32.dll zu laden und dieses Symbol für den Onlinestatus zu verwenden und auch die Symbol-ID 1002 aus diesem Modul zu laden, das für den Offlinestatus verwendet werden soll: `mymod32.dll,#1001,#1002` . Es Outlook in der Statusleiste kein Symbol verwendet. 
  
Wenn keine benutzerdefinierten Symbole angegeben werden, wird der Anbieter standardmäßig durch die Outlook für den Onlinestatus und den Offlinestatus dargestellt. Der Anbieter kann optional einen Anzeigenamen angeben, der neben dem Symbol in der Statusleiste angezeigt werden soll. Weitere Informationen finden Sie **unter PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

