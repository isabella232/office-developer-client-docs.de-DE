---
title: Kanonische Pidtagdefaultviewentryid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270014"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Kanonische Pidtagdefaultviewentryid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID der Standardansicht eines Ordners.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Kennung:  <br/> |0x3616  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist die Eintrags-ID der Ordneransicht, die als Anfangsansicht festgelegt werden soll. Die Eigenschaft muss nicht festgelegt werden, wenn die Ansicht "Normal" als Anfangsansicht verwendet werden soll.
  
Eine Clientanwendung kann diese Eigenschaft zum Zeitpunkt des Öffnens des Ordners abrufen und deutliche Leistungssteigerungen erzielen. Diese Eigenschaft kann als Verknüpfung verwendet werden, um die Standardansicht abzurufen, anstatt die zugehörige Inhaltstabelle zu öffnen und eine Einschränkung zu übermitteln.
  
Eine Dienstanbieterimplementierung der [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) -Methode kann diese Eigenschaft kopieren, wenn Sie Ordner kopiert. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordner Vorgänge.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

