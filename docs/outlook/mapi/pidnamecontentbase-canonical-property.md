---
title: Kanonische PidNameContentBase-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 17c227ecf6451cf5c0b5ca6c8c7fa30c05e0f416
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579285"
---
# <a name="pidnamecontentbase-canonical-property"></a>Kanonische PidNameContentBase-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen [RFC3282] Content-Base-Headerfeldwert.
  
|||
|:-----|:-----|
|Anzeigenamen:  <br/> |BodyContentBase  <br/> |
|Eigenschaftensatz:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Eigenschaftenname:  <br/> |Inhaltsbasis  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um den Wert dieser Eigenschaft festzulegen, müssen MIME-Clients (Multipurpose Internet Message Extensions) den gewünschten Wert in ein Content-Base-Headerfeld einer MIME-Entität schreiben, die einem Nachrichtentext zugeordnet ist. MIME-Leser müssen den Wert eines Content-Base-Headerfelds für eine solche MIME-Entität in den Wert dieser Eigenschaft kopieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

