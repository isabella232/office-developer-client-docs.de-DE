---
title: PidTagSpoolerStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408677"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>PidTagSpoolerStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Status der Nachricht basierend auf Informationen, die für den MAPI-Spooler verfügbar sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Kennung:  <br/> |0x0E10  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht durchlässig  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von MAPI für Nachrichtenobjekte berechnet.
  
Diese Eigenschaft wird nur für eingehende Nachrichten angezeigt und ist in allen anderen Fällen reserviert. Es gibt an, ob eine Nachricht an den endgültigen Speicherort zugestellt wurde oder ob ein Messaging-Hook-Anbieter die Nachricht beim Umleitungsrouting möglicherweise gelöscht hat.
  
Clientanwendungen sollten diese Eigenschaft nie festlegen. Bei einer eingehenden Nachricht kann ein Client oder Dienstanbieter [IMAPIProp::GetProps](imapiprop-getprops.md) für diese Eigenschaft aufrufen, um den Nachrichtenstatus zu bestimmen. Der Wert S_OK an, dass die Nachricht erfolgreich an den Nachrichtenspeicher übermittelt wurde. Der Wert MAPI_E_OBJECT_DELETED an, dass die Nachricht gelöscht wurde und niemals für den Speicher gebunden wurde. 
  
Nachrichtenspeicheranbieter sollten diese Eigenschaft für Nachrichten, Empfängertabellen und die Tabelle für ausgehende Warteschlangen unterstützen. Clients und Anbieter sollten in der Lage sein, Spalten in der Tabelle für ausgehende Warteschlangen zu setzen und basierend auf dieser Eigenschaft einzuschränken.
  
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

