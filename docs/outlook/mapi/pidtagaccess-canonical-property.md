---
title: Kanonische PidTagAccess-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7fb0a4b7ec1ee6d32f30a30a3a319a0ae6c07742
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550848"
---
# <a name="pidtagaccess-canonical-property"></a>Kanonische PidTagAccess-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die die Vorgänge angeben, die dem Client für das Objekt zur Verfügung stehen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACCESS  <br/> |
|Kennung:  <br/> |0x0FF4  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Zugriffssteuerungseigenschaften  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist schreibgeschützt für den Client. Es muss ein **bitweiser OR** von Null oder mehr Werten aus der folgenden Tabelle sein. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Schreiben  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Lesen  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Löschen  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Erstellen von Unterordnern in der Ordnerhierarchie  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Erstellen von Inhaltsnachrichten  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Erstellen zugeordneter Inhaltsnachrichten  <br/> |
   
Die Flags MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY und MAPI_ACCESS_READ befinden sich in Ordner- und Nachrichtenobjekten sowie in der **PR_ACCESS** Spalte in Inhaltstabellen und zugehörigen Inhaltstabellen. Die Flags MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS und MAPI_ACCESS_CREATE_HIERARCHY werden nur für Ordnerobjekte gefunden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

