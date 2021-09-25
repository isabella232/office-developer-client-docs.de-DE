---
title: PidTagRoamingDatatypes (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 87dc35830d237ce98f56f6633251f8d1cd1d0e88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570881"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>PidTagRoamingDatatypes (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske, die angibt, welche Datenstromeigenschaften in der Nachricht vorhanden sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Kennung:  <br/> |0x7C06  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Konfiguration  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft muss auf einen oder mehrere der folgenden Werte festgelegt werden:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000002  <br/> |Gibt an, dass die FaI-Nachricht (Folder Associated Information) einen Wörterbuchdatenstrom enthalten soll, der in ein festes XML-Schema serialisiert und in der **eigenschaft PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) gespeichert wird. Wenn die FAI-Nachricht keinen Wörterbuchdatenstrom enthält, muss die Anwendung das Wörterbuch so behandeln, dass es keine Einträge enthält.  <br/> |
|0x00000004  <br/> |Gibt an, dass die FAI-Nachricht einen XML-Datenstrom enthalten muss, der in der **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) -Eigenschaft gespeichert ist, die ein beliebiges XML-Schema verwendet.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.
    
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

