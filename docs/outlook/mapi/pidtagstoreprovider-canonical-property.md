---
title: Kanonische Pidtagstoreprovider (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278708"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Kanonische Pidtagstoreprovider (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine vom Anbieter definierte [MAPIUID](mapiuid.md) -Struktur, die den Typ des Nachrichtenspeichers angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MDB_PROVIDER  <br/> |
|Kennung:  <br/> |0x3414  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die [MAPIUID](mapiuid.md) -Struktur gibt den Typ des Nachrichtenspeichers an. Der Wert wird von Nachrichtenspeicher Anbietern auf Nachrichtenspeicher Objekten berechnet und ist für jeden Anbieter eindeutig. Sie wird in der Regel zum Durchsuchen der Nachrichtenspeichertabelle verwendet, um einen Speicher des gewünschten Typs zu finden, beispielsweise öffentliche Ordner. 
  
Diese Eigenschaft entspricht der **PR_AB_PROVIDER_ID** ([pidtagabproviderid (](pidtagabproviderid-canonical-property.md))-Eigenschaft für Adressbücher. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

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

