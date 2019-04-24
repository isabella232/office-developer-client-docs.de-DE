---
title: Kanonische Pidtagreadreceiptrequested (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356469"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a>Kanonische Pidtagreadreceiptrequested (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Nachrichtenabsender wünscht, dass das Messagingsystem einen Lesebericht generiert, wenn der Empfänger eine Nachricht gelesen hat.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_READ_RECEIPT_REQUESTED  <br/> |
|Kennung:  <br/> |0x0029  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss auf TRUE festgelegt sein, um die Werte in den Eigenschaften **PR_READ_RECEIPT_ENTRYID** ([Pidtagreadreceiptentryid (](pidtagreadreceiptentryid-canonical-property.md)) und **PR_READ_RECEIPT_SEARCH_KEY** ([pidtagreadreceiptsearchkey (](pidtagreadreceiptsearchkey-canonical-property.md)) zu überprüfen.
  
Wenn eine Nachricht mit **PR_READ_RECEIPT_REQUESTED** -Satz gelöscht oder abgelaufen ist, bevor das Messagingsystem einen Lesebericht generieren kann, wird ein nicht lesbarer Bericht generiert. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

