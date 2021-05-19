---
title: PidNameContentBase (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331500"
---
# <a name="pidnamecontentbase-canonical-property"></a>PidNameContentBase (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen [RFC3282] Content-Base-Headerfeldwert.
  
|||
|:-----|:-----|
|Anzeigenamen:  <br/> |BodyContentBase  <br/> |
|Eigenschaftensatz:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Eigenschaftsname:  <br/> |Content-Base  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>Hinweise

Um den Wert dieser Eigenschaft festlegen zu können, müssen Multipurpose Internet Message Extensions (MIME)-Clients den gewünschten Wert in ein Content-Base-Kopfzeilenfeld für eine MIME-Entität schreiben, die einem Nachrichtentext zu ordnet. MIME-Reader müssen den Wert eines Content-Base-Kopfzeilenfelds für eine solche MIME-Entität in den Wert dieser Eigenschaft kopieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

