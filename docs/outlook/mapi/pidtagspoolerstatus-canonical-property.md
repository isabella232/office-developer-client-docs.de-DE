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
ms.openlocfilehash: d04144a4f5ef714b59b608bfe19367bcb3c1ced8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588573"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>PidTagSpoolerStatus (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält den Status der Nachricht basierend auf Informationen, die für die MAPI-Warteschlange verfügbar ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Kennung:  <br/> |0x0E10  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird auf Message Objekte MAPI berechnet.
  
Diese Eigenschaft wird auf eingehende Nachrichten nur angezeigt und ist in allen anderen Fällen reserviert. Es gibt an, unabhängig davon, ob eine Nachricht an seinem endgültigen Speicherort übermittelt wurde, oder gibt an, ob ein messaging Hook Anbieter potenziell die Nachricht beim gelöscht erneutes es.
  
Clientanwendungen sollten diese Eigenschaft festlegen. Für eine eingehende Nachricht kann ein Client oder Dienstanbieter [IMAPIProp::GetProps](imapiprop-getprops.md) für diese Eigenschaft zum Bestimmen des Nachrichtenstatus aufrufen. Der Wert S_OK gibt an, dass die Nachricht erfolgreich an den Nachrichtenspeicher übermittelt wurde. Der Wert MAPI_E_OBJECT_DELETED gibt an, dass die Nachricht gelöscht wurde und an den Store nie zugesichert wurde. 
  
Nachricht Anbieter sollte diese Eigenschaft auf Nachrichten, Empfänger Tabellen und der ausgehende Warteschlangentabelle unterstützen. Clients und Anbieter sollte können Spalten in der ausgehenden Warteschlangentabelle festgelegt und einschränken können basierend auf dieser Eigenschaft.
  
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

