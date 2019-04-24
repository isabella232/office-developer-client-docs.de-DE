---
title: Kanonische PidTagTitle-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTitle
api_type:
- COM
ms.assetid: f35bbcc3-15dd-40ab-9bf4-bdb21f95d464
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2501ea7c4be08b0bec3c2d65e6a504df47dfc488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358765"
---
# <a name="pidtagtitle-canonical-property"></a>Kanonische PidTagTitle-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Position des Empfängers.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_TITLE, PR_TITLE_A, PR_TITLE_W  <br/> |
|Kennung:  <br/> |0x3A17  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-e-Mail-Benutzer  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften bieten Identifizierungs-und Zugriffsinformationen für einen Empfänger. Sie werden vom Empfänger und der Organisation des Empfängers definiert. 
  
Diese Eigenschaften werden häufig verwendet, um die formale Position des Empfängers, wie beispielsweise Senior Programmierer, anstelle der berufsklasse, wie zum Beispiel Programmierer, anzugeben. Sie wird in der Regel nicht für Suffix-Titel wie Esq verwendet. oder DDS.
  
Zu den allgemeinen Werten für diese Eigenschaft gehört: Managing Director, Programmer II, Associate Professor und Development Lead. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
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

