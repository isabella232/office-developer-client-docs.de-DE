---
title: Kanonische Pidtagpstpathhint (-Eigenschaft
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
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437308"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Kanonische Pidtagpstpathhint (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt den Namen der persönlichen Speichertabelle (PST-Datei) bereit, den der Benutzer bearbeiten kann, für das Dialogfeld Konfiguration. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Kennung:  <br/> |0x6771  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Persönliche Speichertabelle (PST) intern  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn stattdessen die **PR_PST_PATH** ([pidtagpstpath (](pidtagpstpath-canonical-property.md))-Eigenschaft verwendet wird, wird das Dialogfeld Konfiguration geöffnet, aber der Benutzer kann den Pfad und viele andere Eigenschaften nicht bearbeiten.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

