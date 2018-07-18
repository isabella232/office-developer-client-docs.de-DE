---
title: PidNameRightsManagementLicense (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793995"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>PidNameRightsManagementLicense (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Speichert die Lizenz für die rechteverwaltung e-Mail-Nachricht.
  
|||
|:-----|:-----|
|Anzeigenamen:  <br/> |Keine  <br/> |
|-Eigenschaft festgelegt:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Name der Eigenschaft:  <br/> |DRMLicense  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Sichere Nachrichten  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Eigenschaft auf eine e-Mail mit verwalteten rechten vorhanden ist, muss der erste Wert dieser Eigenschaft für mehrere binäre komprimierte Nutzungslizenz ZLIB (wie in [RFC1950] angegeben) für die rechteverwaltung e-Mail-Nachricht enthalten.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

