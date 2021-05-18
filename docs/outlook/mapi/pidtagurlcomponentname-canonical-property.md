---
title: PidTagUrlComponentName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320426"
---
# <a name="pidtagurlcomponentname-canonical-property"></a>PidTagUrlComponentName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Name der URL-Komponente für eine Nachricht. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W  <br/> |
|Kennung:  <br/> |0x10F3  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sollten innerhalb eines Ordners eindeutig sein. Wenn beim Erstellen der Nachricht nicht festgelegt wird, sollte der Nachrichtenspeicher diese Eigenschaften basierend auf verschiedenen Nachrichteneigenschaften abhängig von der Nachrichtenklasse festlegen. Beispiel: **IPM. Hinweis** und **IPM. Terminnachrichten** sollten diese Eigenschaft basierend auf der **eigenschaft PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **dem IPM festlegen. Für** Kontaktnachrichten sollte diese Eigenschaft basierend auf der **eigenschaft dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) festgelegt werden. Für die meisten anderen Nachrichtenklassen sollte diese Eigenschaft auf der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) basieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

