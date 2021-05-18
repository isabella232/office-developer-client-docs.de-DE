---
title: PidTagAttachPayloadProviderGuidString (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361103"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>PidTagAttachPayloadProviderGuidString (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert eines MIME X-Payload-Provider-Guid-Headerfelds.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W  <br/> |
|Kennung:  <br/> |0x3719  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Hinweise

Zum Festlegen des Werts dieser Eigenschaften sollten MIME-Clients ein X-Payload-Provider-Guid-Headerfeld in eine MIME-Entität schreiben, die als Anlage analysiert wird.
  
MIME-Reader müssen diesen Headerfeldwert in den Wert der entsprechenden Eigenschaft kopieren. MIME-Leser sollten dieses Kopfzeilenfeld ignorieren, wenn es in einer MIME-Entität angezeigt wird, die als Nachrichten- oder Nachrichtentext und nicht als Anlage analysiert wird.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
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

