---
title: Kanonische Pidtagprovidericon (-Eigenschaft
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
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286460"
---
# <a name="pidtagprovidericon-canonical-property"></a>Kanonische Pidtagprovidericon (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Unicode-Zeichenfolge, die ein benutzerdefiniertes Symbol oder Symbole angibt, die für einen MAPI-Anbieter in der Microsoft Office Outlook-Statusleiste in Online-und Offline Zuständen angezeigt werden sollen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Kennung:  <br/> |0x3417  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften geben die Ressourcendatei an, die ein benutzerdefiniertes Symbol enthält, das einen MAPI-Anbieter in einem Onlinestatus darstellt, und optional ein weiteres benutzerdefiniertes Symbol im Offlinestatus. Diese Eigenschaften werden von Outlook immer in der Unicode-Darstellung angefordert. 
  
Der folgende Eigenschaftswert weist beispielsweise Outlook an, die Symbol-ID 1001 aus dem Modul mymod32. dll zu laden und dieses Symbol für den Online `mymod32.dll,#1001`Status zu verwenden:. Da es kein anbieterspezifisches Symbol für den Offlinestatus gibt, wird in diesem Fall das Standardsymbol Outlook offline in der Statusleiste verwendet. 
  
Der folgende Eigenschaftswert weist Outlook an, die Symbol-ID 1001 aus dem Modul mymod32. dll zu laden und dieses Symbol für den Onlinestatus zu verwenden und auch die Symbol-ID 1002 aus demselben Modul zu laden, das für `mymod32.dll,#1001,#1002`den Offlinestatus verwendet werden soll:. In der Statusleiste wird kein Outlook-Symbol verwendet. 
  
Wenn keine benutzerdefinierten Symbole angegeben werden, wird der Anbieter standardmäßig durch die Outlook-Standardsymbole für den Status Online und den Status Offline dargestellt. Der Anbieter kann optional einen Anzeigenamen angeben, der neben dem Symbol in der Statusleiste angezeigt werden soll. Weitere Informationen finden Sie unter **PR_PROVIDER_DISPLAY_NAME_W** ([pidtagproviderdisplayname (](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

