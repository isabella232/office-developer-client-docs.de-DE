---
title: Kanonische Pidlidtaskmultiplerecipients (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360067"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>Kanonische Pidlidtaskmultiplerecipients (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Optimierungshinweise zu den Empfängern einer Aufgabe.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskMultRecips  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long-ID (Deckel):  <br/> |0x00008120  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft festgelegt ist, muss Sie auf eine bitweise **or** -Operation mit 0 oder mehr der folgenden Werte festgelegt werden. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|Gesendet  <br/> |0x00000001  <br/> |Die Aufgabe hat mehrere primäre Empfänger.  <br/> |
|Auszahlung  <br/> |0x00000002  <br/> |Obwohl der gesendete Hinweis nicht vorhanden war, erkannte der Client, dass die Aufgabe mehrere primäre Empfänger hat.  <br/> |
|Reserved  <br/> |0x00000004  <br/> |Dieser Wert ist reserviert.  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

