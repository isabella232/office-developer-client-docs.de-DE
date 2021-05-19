---
title: PidLidSpamOriginalFolder (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331556"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a>PidLidSpamOriginalFolder (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, in welchem Ordner sich eine Nachricht befindet, bevor sie in den Junk-E-Mail-Ordner gefiltert wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSpamOriginalFolder  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x0000859C  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist die **EntryID** des Ordners, der die Nachricht enthielt, bevor sie verschoben wurde. Diese Eigenschaft sollte festgelegt werden, wenn eine Nachricht als Spam gekennzeichnet ist. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

