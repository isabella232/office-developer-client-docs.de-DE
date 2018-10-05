---
title: PidTagDefaultViewEntryId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393516"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>PidTagDefaultViewEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID der Standardansicht für einen Ordner.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Kennung:  <br/> |0x3616  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist die Eintrags-ID der Ordneransicht, die als Standardansicht festgelegt werden soll. Die Eigenschaft muss nicht festgelegt werden, wenn die Ansicht "Normal" als Standardansicht verwendet werden.
  
Eine Clientanwendung diese Eigenschaft zum Zeitpunkt geöffnet wird den Ordner abrufen und erhebliche Leistungsvorteile erzielt. Diese Eigenschaft kann als eine Verknüpfung zum Abrufen der Standardansicht, anstatt die zugeordneten Inhaltstabelle öffnen, und senden Sie eine Einschränkung von verwendet werden.
  
Die Implementierung einer Service Provider der [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) -Methode kann diese Eigenschaft kopieren, wenn Ordner kopiert. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Ordner Vorgänge behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

