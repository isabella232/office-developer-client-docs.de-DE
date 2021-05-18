---
title: PidTagAccess (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316513"
---
# <a name="pidtagaccess-canonical-property"></a>PidTagAccess (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die die Vorgänge angibt, die dem Client für das Objekt zur Verfügung stehen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACCESS  <br/> |
|Kennung:  <br/> |0x0FF4  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Eigenschaften der Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt für den Client. Es muss ein bitweises **OR** von null oder mehr Werten aus der folgenden Tabelle sein. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Schreiben  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Lesen  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Löschen  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Erstellen von Unterordnern in der Ordnerhierarchie  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Erstellen von Inhaltsnachrichten  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Erstellen zugeordneter Inhaltsnachrichten  <br/> |
   
Die MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY und MAPI_ACCESS_READ werden in Ordner- und Nachrichtenobjekten und in der spalte **PR_ACCESS** in Inhaltstabellen und zugehörigen Inhaltstabellen gefunden. Die MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS und MAPI_ACCESS_CREATE_HIERARCHY werden nur für Ordnerobjekte gefunden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

