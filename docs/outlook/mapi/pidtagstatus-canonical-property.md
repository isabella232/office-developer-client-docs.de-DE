---
title: Kanonische PidTagStatus-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68ab44134fd26f4a29b3048126bae73bf4dd0c82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599410"
---
# <a name="pidtagstatus-canonical-property"></a>Kanonische PidTagStatus-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine 32-Bit-Bitmaske mit Flags, die den Ordnerstatus definieren.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS  <br/> |
|Kennung:  <br/> |0x360B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft für Ordner entspricht der **eigenschaft PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) für Nachrichten. Die Flags werden nur für die Clientanwendung bereitgestellt und wirken sich nicht auf den Nachrichtenspeicher aus. Clients können diese Einstellungen verwenden oder ignorieren. Der Client kann auch eigene Werte für die clientdefinierbaren Bits dieser Eigenschaft definieren.
  
Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:
  
FLDSTATUS_DELMARKED 
  
> Der Ordner wird zum Löschen markiert. Die Clientanwendung legt dieses Kennzeichen fest.
    
FLDSTATUS_HIDDEN 
  
> Der Ordner ist ausgeblendet.
    
FLDSTATUS_HIGHLIGHTED 
  
> Der Ordner wird hervorgehoben, z. B. im umgekehrten Video.
    
FLDSTATUS_TAGGED 
  
> Der Ordner ist markiert.
    
Nachrichtenspeicheranbieter legen diese Eigenschaft für einen Ordner auf einen oder mehrere dieser Werte fest, und Clients interpretieren den Status entsprechend ihren Anwendungen. Beispielsweise kann ein Client den Ordnerstatus verwenden, um zwischen Ordnern in einer Hierarchietabelle visuell zu unterscheiden und Ordner mit demselben Status auf die gleiche Weise anzuzeigen. Hervorgehobene Ordner können im umgekehrten Video angezeigt werden, markierte Ordner und Ordner, die für den Löschvorgang markiert sind, können mit einem aussagekräftigen Symbol angezeigt werden, und ausgeblendete Ordner können ausgeblendet werden.
  
Die Bits 16 bis 31 ("0x10000" bis "0x80000000") dieser Eigenschaft sind für die Verwendung durch die IPM-Clientanwendung verfügbar. Alle anderen Bits sind für die Verwendung durch MAPI reserviert. Diejenigen, die nicht in der vorherigen Liste definiert sind, sollten anfänglich auf Null festgelegt und nicht geändert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

