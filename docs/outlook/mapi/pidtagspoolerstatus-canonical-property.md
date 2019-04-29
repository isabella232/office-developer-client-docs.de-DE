---
title: Kanonische Pidtagspoolerstatus (-Eigenschaft
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
# <a name="pidtagspoolerstatus-canonical-property"></a>Kanonische Pidtagspoolerstatus (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Status der Nachricht basierend auf Informationen, die dem MAPI-Spooler zur Verfügung stehen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Kennung:  <br/> |0x0E10  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nicht transmitable MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird von MAPI für Nachrichtenobjekte berechnet.
  
Diese Eigenschaft wird nur für eingehende Nachrichten angezeigt und ist in allen anderen Fällen reserviert. Er gibt an, ob eine Nachricht an ihren endgültigen Standort übermittelt wurde oder ob ein nachrichtenverbindungs Anbieter die Nachricht möglicherweise beim erneuten Routing gelöscht hat.
  
Client Anwendungen sollten diese Eigenschaft nie festlegen. Für eine eingehende Nachricht kann ein Client oder Dienstanbieter [IMAPIProp::](imapiprop-getprops.md) GetProps für diese Eigenschaft aufrufen, um den Nachrichtenstatus zu bestimmen. Der Wert S_OK gibt an, dass die Nachricht erfolgreich an den Nachrichtenspeicher übermittelt wurde. Der Wert MAPI_E_OBJECT_DELETED gibt an, dass die Nachricht gelöscht wurde und nie an den Speicher übergeben wurde. 
  
Nachrichtenspeicher Anbieter sollten diese Eigenschaft für Nachrichten, Empfänger Tabellen und die Tabelle für ausgehende Warteschlangen unterstützen. Clients und Anbieter sollten in der Lage sein, Spalten der ausgehenden Warteschlangentabelle festzulegen und basierend auf dieser Eigenschaft einzuschränken.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

