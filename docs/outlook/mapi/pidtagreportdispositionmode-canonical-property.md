---
title: PidTagReportDispositionMode (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 67b3c76a-f6f7-462b-955c-dc7b53e7e7eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b16cf3b8d0281ba8995058af6b18dbe22dcf592
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566117"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a>PidTagReportDispositionMode (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zeigt die Disposition des Eingangs für Nachrichten, die Empfangsbestätigungen anfordern. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W  <br/> |
|Kennung:  <br/> |0x0081  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die möglichen Werte für diese Eigenschaft sind "manuell-Aktion/MDN-gesendet-automatisch" und "manuell-Aktion/MDN-gesendet-manuell".
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
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

