---
title: PidTagProviderIcon (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4eb349be279196ecbdf30bafa698e2b0773f6a6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599698"
---
# <a name="pidtagprovidericon-canonical-property"></a>PidTagProviderIcon (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicode-Zeichenfolge, die ein benutzerdefiniertes Symbol oder Symbole angibt, das für einen MAPI-Anbieter in der Microsoft Office Outlook Statusleiste sowohl im Online- als auch im Offlinestatus angezeigt werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Kennung:  <br/> |0x3417  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften geben die Ressourcendatei an, die ein benutzerdefiniertes Symbol enthält, das einen MAPI-Anbieter in einem Onlinestatus darstellt, und optional ein weiteres benutzerdefiniertes Symbol im Offlinestatus. Outlook fordert diese Eigenschaften immer in Unicode-Darstellung an. 
  
Beispielsweise weist der folgende Eigenschaftswert Outlook an, die Symbol-ID 1001 aus dem Modul mymod32.dll zu laden und dieses Symbol für den Onlinestatus zu verwenden: `mymod32.dll,#1001` . Da kein anbieterspezifisches Symbol für den Offlinestatus vorhanden ist, wird in diesem Fall das standardmäßige Outlook Offlinesymbol in der Statusleiste verwendet. 
  
Der folgende Eigenschaftswert weist Outlook an, die Symbol-ID 1001 aus dem Modul mymod32.dll zu laden und dieses Symbol für den Onlinestatus zu verwenden sowie die Symbol-ID 1002 aus demselben Modul zu laden, das für den Offlinestatus verwendet werden soll: `mymod32.dll,#1001,#1002` . In der Statusleiste wird kein Outlook Symbol verwendet. 
  
Wenn keine benutzerdefinierten Symbole angegeben sind, wird der Anbieter standardmäßig durch die Outlook Standardsymbole für den Onlinestatus und den Offlinestatus dargestellt. Der Anbieter kann optional einen Anzeigenamen angeben, der neben dem Symbol in der Statusleiste angezeigt werden soll. Weitere Informationen finden Sie unter **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

