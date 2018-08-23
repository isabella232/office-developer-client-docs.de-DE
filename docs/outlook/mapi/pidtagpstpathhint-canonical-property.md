---
title: PidTagPstPathHint (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6b71feb6d5967eab3aa490a256825a2803381f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569092"
---
# <a name="pidtagpstpathhint-canonical-property"></a>PidTagPstPathHint (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen der persönlicher Speicher-Tabelle (PST-Datei), die der Benutzer bearbeiten können, für das Dialogfeld Konfiguration. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Kennung:  <br/> |0x6771  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Persönlicher Speicher-Tabelle (. pst) interne  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie stattdessen die **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md))-Eigenschaft verwendet wird, im Dialogfeld Konfiguration wird geöffnet, aber der Benutzer kann nicht den Pfad und viele andere Eigenschaften bearbeiten.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
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

