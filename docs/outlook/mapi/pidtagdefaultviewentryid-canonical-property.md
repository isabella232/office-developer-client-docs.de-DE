---
title: PidTagDefaultViewEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da4384846eb139246b62f7beaae75066288ceb9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600267"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>PidTagDefaultViewEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner der Standardansicht eines Ordners.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Kennung:  <br/> |0x3616  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist der Eintragsbezeichner der Ordneransicht, die als Ausgangsansicht festgelegt werden soll. Die Eigenschaft muss nicht festgelegt werden, wenn die "Normal"-Ansicht als Ausgangsansicht verwendet werden soll.
  
Eine Clientanwendung kann diese Eigenschaft zum Zeitpunkt des Öffnens des Ordners abrufen und erhebliche Leistungsvorteile erzielen. Diese Eigenschaft kann als Verknüpfung verwendet werden, um die Standardansicht abzurufen, anstatt das zugeordnete Inhaltsverzeichnis zu öffnen und eine Einschränkung zu übermitteln.
  
Eine Dienstanbieterimplementierungen der [IMAPIFolder::CopyFolder-Methode](imapifolder-copyfolder.md) können diese Eigenschaft beim Kopieren von Ordnern kopieren. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordnervorgänge.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

