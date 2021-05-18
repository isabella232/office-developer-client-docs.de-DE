---
title: PidTagRoamingDatatypes (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359556"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>PidTagRoamingDatatypes (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske, die angibt, welche Streameigenschaften in der Nachricht vorhanden sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Kennung:  <br/> |0x7C06  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Konfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft muss auf einen oder mehrere der folgenden Werte festgelegt werden:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000002  <br/> |Gibt an, dass die #A0 (Folder Associated Information) einen Dictionary-Stream enthalten soll, der in ein festes **#A1** serialisiert und in der PR_ROAMING_DICTIONARY ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md))-Eigenschaft gespeichert ist. Wenn die FAI-Nachricht keinen Dictionary-Stream enthält, muss die Anwendung das Wörterbuch als einträgelos behandeln.  <br/> |
|0x00000004  <br/> |Gibt an, dass die #A0 einen #A1 **enthalten muss,** der in der PR_ROAMING_XMLSTREAM ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md))-Eigenschaft gespeichert ist, die ein beliebiges #A1 verwendet.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.
    
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

