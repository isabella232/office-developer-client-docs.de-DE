---
title: Kanonische PidTagSensitivity-Eigenschaft
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
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342504"
---
# <a name="pidtagsensitivity-canonical-property"></a>Kanonische PidTagSensitivity-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der die Meinung des Nachrichtenabsenders zur Vertraulichkeit einer Nachricht angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SENSITIVITY  <br/> |
|Kennung:  <br/> |0x0036  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Nachrichtenobjekte diese Eigenschaft verfügbar machen.
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
SENSITIVITY_NONE 
  
> Die Nachricht hat keine besondere Vertraulichkeit.
    
SENSITIVITY_PERSONAL 
  
> Die Nachricht ist persönlich.
    
SENSITIVITY_PRIVATE 
  
> Die Nachricht ist privat.
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> Die Nachricht wird als "Company Confidential" festgelegt.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
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

