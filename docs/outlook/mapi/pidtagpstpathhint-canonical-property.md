---
title: PidTagPstPathHint (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e2407a9efdf43a7a83418e1ab77e1054ac3b954b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574797"
---
# <a name="pidtagpstpathhint-canonical-property"></a>PidTagPstPathHint (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt den Namen der persönlichen Speichertabelle (PST-Datei) für das Konfigurationsdialogfeld bereit, den der Benutzer bearbeiten kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Kennung:  <br/> |0x6771  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Persönliche Speichertabelle (PST) intern  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn stattdessen die **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) -Eigenschaft verwendet wird, wird das Konfigurationsdialogfeld geöffnet, aber der Benutzer kann den Pfad und viele andere Eigenschaften nicht bearbeiten.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

