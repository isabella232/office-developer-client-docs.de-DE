---
title: Kanonische PidTagStoreProvider-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c16f2477d107220408771328f4ad339774a696cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599375"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Kanonische PidTagStoreProvider-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine vom Anbieter definierte [MAPIUID-Struktur,](mapiuid.md) die den Typ des Nachrichtenspeichers angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MDB_PROVIDER  <br/> |
|Kennung:  <br/> |0x3414  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die [MAPIUID-Struktur](mapiuid.md) identifiziert den Typ des Nachrichtenspeichers. Der Wert wird von Nachrichtenspeicheranbietern für Nachrichtenspeicherobjekte berechnet und ist für jeden Anbieter eindeutig. Es wird in der Regel zum Durchsuchen der Nachrichtenspeichertabelle verwendet, um einen Speicher des gewünschten Typs zu finden, z. B. öffentliche Ordner. 
  
Diese Eigenschaft entspricht der **eigenschaft PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) für Adressbücher. 
  
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

