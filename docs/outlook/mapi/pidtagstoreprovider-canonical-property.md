---
title: PidTagStoreProvider (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412051"
---
# <a name="pidtagstoreprovider-canonical-property"></a>PidTagStoreProvider (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine vom Anbieter definierte [MAPIUID-Struktur,](mapiuid.md) die den Typ des Nachrichtenspeichers angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MDB_PROVIDER  <br/> |
|Kennung:  <br/> |0x3414  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Die [MAPIUID-Struktur](mapiuid.md) identifiziert den Typ des Nachrichtenspeichers. Der Wert wird von Nachrichtenspeicheranbietern für Nachrichtenspeicherobjekte berechnet und ist für jeden Anbieter eindeutig. Es wird in der Regel zum Durchsuchen der Tabelle des Nachrichtenspeichers verwendet, um einen Speicher des gewünschten Typs zu finden, z. B. öffentliche Ordner. 
  
Diese Eigenschaft entspricht der PR_AB_PROVIDER_ID **(** [PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) -Eigenschaft für Adressbücher. 
  
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

