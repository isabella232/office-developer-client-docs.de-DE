---
title: PidTagImplicitConversionProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7635dd24f4fbc5128d3d96556802ab2e3fe56e35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571843"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>PidTagImplicitConversionProhibited (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält True, wenn ein Message Transfer Agent (MTA) tätigen implizite Nachricht Text Konvertierungen verboten wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Kennung:  <br/> |0x0016  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft auf true festgelegt ist, muss das messaging-System keine inhaltskonvertierung für die Nachricht ausführen, wenn es für eine einzelne pro Empfänger mit der **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md))-Eigenschaft explizit angefordert wird.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

