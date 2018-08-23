---
title: PidTagIpmWastebasketEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66bbf49d737c42ecc2f6c765a60540163649f447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573894"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a>PidTagIpmWastebasketEntryId (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des Ordners "Gelöschte Elemente standard zwischen Personen Nachricht (IPM)". 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IPM_WASTEBASKET_ENTRYID  <br/> |
|Kennung:  <br/> |0x35E3  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung sollte gelöschte Nachrichten zwischen Personen in den Ordner Gelöschte Objekte verschieben. Wenn die Nachricht bereits in diesem Ordner befindet, oder wenn diese Eigenschaft nicht unterstützt wird, sollte der Client die Nachricht zu löschen. 
  
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

