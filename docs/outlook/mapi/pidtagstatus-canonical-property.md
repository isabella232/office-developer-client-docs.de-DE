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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 01a65306e5e0d34ed6f1ce7231227224868ff5cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795208"
---
# <a name="pidtagstatus-canonical-property"></a>PidTagStatus (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine 32-Bit-Bitmaske aus Flags, die Ordner Status definieren.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_STATUS  <br/> |
|Bezeichner:  <br/> |0x360B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-container  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft für Ordner entspricht der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft für Nachrichten. Ihre Flags werden für die Client-Anwendung bereitgestellt und wirken sich nicht auf den Nachrichtenspeicher. Clients verwenden oder ignorieren diese Einstellungen. Der Client kann auch eine eigene Werte für die Client-definierbare Bit dieser Eigenschaft definieren.
  
Für die Bitmaske kann eine oder mehrere der folgenden Werte festgelegt werden:
  
FLDSTATUS_DELMARKED 
  
> Der Ordner ist zum Löschen gekennzeichnet. Die Client-Anwendung wird dieses Flag.
    
FLDSTATUS_HIDDEN 
  
> Der Ordner ist ausgeblendet.
    
FLDSTATUS_HIGHLIGHTED 
  
> Der Ordner ist, beispielsweise markiert in umgekehrter Reihenfolge video dargestellt.
    
FLDSTATUS_TAGGED 
  
> Der Ordner gekennzeichnet ist.
    
Nachricht Anbieter legen Sie diese Eigenschaft auf einen Ordner auf eine oder mehrere der folgenden Werte und Clients Interpretieren des Status nach Bedarf für eine Anwendung. Angenommen, können ein Client den Ordner Status Sie hervorheben zwischen Ordnern in einer Hierarchietabelle, Anzeigen von Ordnern mit dem gleichen Status auf die gleiche Weise verwendet. Markierten Ordner in umgekehrter video, markierte Ordner angezeigt werden können und Ordnern zum Löschen markiert mit einem aussagekräftigen Symbol angezeigt werden können und verborgene Ordner verborgen werden können.
  
Bits 16 bis 31 ("0 x 10000" durch "0 x 80000000") dieser Eigenschaft stehen für die Verwendung durch die IPM-Clientanwendung. Alle anderen Bits sind MAPI für die Verwendung reserviert. die nicht in der obigen Liste definierten sollte anfänglich auf 0 (null) festgelegt und nicht geändert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

