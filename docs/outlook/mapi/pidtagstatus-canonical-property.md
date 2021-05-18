---
title: PidTagStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278792"
---
# <a name="pidtagstatus-canonical-property"></a>PidTagStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine 32-Bit-Bitmaske mit Flags, die den Ordnerstatus definieren.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS  <br/> |
|Kennung:  <br/> |0x360B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft für Ordner entspricht der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) -Eigenschaft für Nachrichten. Die Flags werden nur für die Clientanwendung bereitgestellt und wirken sich nicht auf den Nachrichtenspeicher aus. Clients können diese Einstellungen verwenden oder ignorieren. Der Client kann auch eigene Werte für die clientdefinierbaren Bits dieser Eigenschaft definieren.
  
Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:
  
FLDSTATUS_DELMARKED 
  
> Der Ordner wird zum Löschen markiert. Die Clientanwendung legt dieses Flag fest.
    
FLDSTATUS_HIDDEN 
  
> Der Ordner ist ausgeblendet.
    
FLDSTATUS_HIGHLIGHTED 
  
> Der Ordner wird z. B. im Umgekehrten Video hervorgehoben.
    
FLDSTATUS_TAGGED 
  
> Der Ordner ist markiert.
    
Nachrichtenspeicheranbieter legen diese Eigenschaft für einen Ordner auf einen oder mehrere dieser Werte festgelegt, und Clients interpretieren den Status entsprechend ihren Anwendungen. Ein Client kann z. B. den Ordnerstatus verwenden, um visuell zwischen Ordnern in einer Hierarchietabelle zu unterscheiden, und Ordner mit demselben Status auf die gleiche Weise anzeigen. Hervorgehobene Ordner können im Reversevideo angezeigt werden, markierte Ordner und Ordner, die zum Löschen markiert sind, können mit einem aussagekräftigen Symbol angezeigt werden, und ausgeblendete Ordner können ausgeblendet werden.
  
Bits 16 bis 31 ("0x10000" bis "0x80000000") dieser Eigenschaft stehen für die Verwendung durch die IPM-Clientanwendung zur Verfügung. Alle anderen Bits sind für die Verwendung durch MAPI reserviert. Diejenigen, die in der vorherigen Liste nicht definiert sind, sollten zunächst auf Null festgelegt und nicht geändert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

