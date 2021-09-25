---
title: PidTagSpoolerStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 473f2745a6c3019db4994192fa4b138f1298b6cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591409"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>PidTagSpoolerStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Status der Nachricht basierend auf Informationen, die für den MAPI-Spooler verfügbar sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Kennung:  <br/> |0x0E10  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird von der MAPI für Nachrichtenobjekte berechnet.
  
Diese Eigenschaft wird nur für eingehende Nachrichten angezeigt und ist in allen anderen Fällen reserviert. Es gibt an, ob eine Nachricht an ihren endgültigen Speicherort übermittelt wurde oder ob ein Messaging-Hookanbieter die Nachricht möglicherweise gelöscht hat, während sie umgeleitet wurde.
  
Clientanwendungen sollten diese Eigenschaft niemals festlegen. Für eine eingehende Nachricht kann ein Client oder Dienstanbieter [IMAPIProp::GetProps](imapiprop-getprops.md) für diese Eigenschaft aufrufen, um den Nachrichtenstatus zu ermitteln. Der Wert S_OK gibt an, dass die Nachricht erfolgreich an den Nachrichtenspeicher übermittelt wurde. Der Wert MAPI_E_OBJECT_DELETED gibt an, dass die Nachricht gelöscht wurde und nie in den Speicher übergeben wurde. 
  
Nachrichtenspeicheranbieter sollten diese Eigenschaft für Nachrichten, Empfängertabellen und die Tabelle für ausgehende Warteschlangen unterstützen. Clients und Anbieter sollten in der Lage sein, Spalten in der Tabelle für ausgehende Warteschlangen festzulegen und basierend auf dieser Eigenschaft einzuschränken.
  
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

