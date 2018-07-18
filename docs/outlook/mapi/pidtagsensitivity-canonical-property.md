---
title: PidTagSensitivity (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 93be3351749ac3e9d285fb214f746d58b55fb5b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795144"
---
# <a name="pidtagsensitivity-canonical-property"></a>PidTagSensitivity (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält einen Wert, der den Nachrichtenabsender Opinion, der die Vertraulichkeit einer Nachricht angibt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SENSITIVITY  <br/> |
|Bezeichner:  <br/> |0x0036  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Message Objekte diese Eigenschaft verfügbar machen.
  
Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
SENSITIVITY_NONE 
  
> Die Nachricht weist keine besondere Vertraulichkeit.
    
SENSITIVITY_PERSONAL 
  
> Die Nachricht ist persönlich.
    
SENSITIVITY_PRIVATE 
  
> Die Nachricht ist privat.
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> Die Nachricht wird Firma (vertraulich) festgelegt.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

