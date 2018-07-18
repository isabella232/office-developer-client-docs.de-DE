---
title: PidLidTaskMultipleRecipients (kanonische Eigenschaft)
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
ms.openlocfilehash: 1e1cba3d927072cb03dbd34eee518c9b0a9e0383
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793847"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>PidLidTaskMultipleRecipients (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält Tipps zum die Empfänger eines Vorgangs Optimierung.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskMultRecips  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008120  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie festlegen möchten, muss diese Eigenschaft auf eine bitweise **OR** -Operation 0 (null) oder mehreren der folgenden Werte festgelegt werden. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|Gesendet  <br/> |0x00000001  <br/> |Der Vorgang hat mehrere primäre Empfänger.  <br/> |
|Auszahlung  <br/> |0x00000002  <br/> |Obwohl die gesendete Hint nicht vorhanden war, erkannt der Client, dass der Vorgang mehrere primäre Empfänger.  <br/> |
|Reserviert  <br/> |0 x 00000004  <br/> |Dieser Wert ist reserviert.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

