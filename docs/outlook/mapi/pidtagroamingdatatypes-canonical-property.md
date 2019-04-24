---
title: Kanonische Pidtagroamingdatatypes (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359556"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>Kanonische Pidtagroamingdatatypes (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske, die angibt, welche Stream-Eigenschaften in der Nachricht vorhanden sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Kennung:  <br/> |0x7C06  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Konfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss auf einen oder mehrere der folgenden Werte festgelegt werden:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000002  <br/> |Gibt an, dass die Nachricht "Folder Associated Information" (FAI) einen Wörterbuchdaten Strom enthalten soll, der in ein festes XML-Schema serialisiert und in der **PR_ROAMING_DICTIONARY** ([pidtagroamingdictionary (](pidtagroamingdictionary-canonical-property.md))-Eigenschaft gespeichert ist. Wenn die FAI-Nachricht keinen Wörterbuchdaten Strom enthält, muss die Anwendung das Wörterbuch als keine Einträge behandeln.  <br/> |
|0x00000004  <br/> |Gibt an, dass die FAI-Nachricht einen in der **PR_ROAMING_XMLSTREAM** ([pidtagroamingxmlstream (](pidtagroamingxmlstream-canonical-property.md))-Eigenschaft gespeicherten XML-Stream enthalten muss, der ein beliebiges XML-Schema verwendet.  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client-und Serverkonfigurationsdaten an, wie beispielsweise Listen mit freigegebenen Kategorien und Arbeitszeiten.
    
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

