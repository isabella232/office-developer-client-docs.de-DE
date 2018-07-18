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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d8b4df2dbb0d7fd2edeb82222f333c11c5f71987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794990"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>PidTagRoamingDatatypes (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske dar, die angibt, welche Stream Eigenschaften für die Nachricht vorhanden sind.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Bezeichner:  <br/> |0x7C06  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Konfiguration  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss auf eine oder mehrere der folgenden Werte festgelegt werden:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000002  <br/> |Gibt an, dass die Nachricht Ordner verknüpften Informationen (FAI) einen Wörterbuch-Stream in einem festen XML-Schema serialisiert und in der Eigenschaft **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) gespeichert enthalten soll. Wenn FAI-Nachricht keinen Wörterbuch Stream enthält, muss die Anwendung das Wörterbuch behandelt, als müssen keine Einträge.  <br/> |
|0 x 00000004  <br/> |Gibt an, dass die Nachricht FAI in die **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md))-Eigenschaft, die eine beliebige XML-Schema verwendet gespeicherten XML-Stream enthalten muss.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.
    
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

