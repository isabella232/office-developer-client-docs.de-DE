---
title: Kanonische Pidtagstatus (-Eigenschaft
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
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278792"
---
# <a name="pidtagstatus-canonical-property"></a>Kanonische Pidtagstatus (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine 32-Bit-Bitmaske von Flags, die den Ordner Status definieren.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STATUS  <br/> |
|Kennung:  <br/> |0x360B  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft für Ordner ist analog zur **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft für Nachrichten. Die zugehörigen Flags werden nur für die Clientanwendung bereitgestellt und wirken sich nicht auf den Nachrichtenspeicher aus. Diese Einstellungen können von Clients verwendet oder ignoriert werden. Der Client kann auch eigene Werte für die vom Client definierbaren Bits dieser Eigenschaft definieren.
  
Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:
  
FLDSTATUS_DELMARKED 
  
> Der Ordner ist zum Löschen markiert. Die Clientanwendung legt dieses Flag fest.
    
FLDSTATUS_HIDDEN 
  
> Der Ordner ist ausgeblendet.
    
FLDSTATUS_HIGHLIGHTED 
  
> Der Ordner wird beispielsweise in "Reverse Video" angezeigt.
    
FLDSTATUS_TAGGED 
  
> Der Ordner ist markiert.
    
Nachrichtenspeicher Anbieter legen diese Eigenschaft für einen Ordner auf einen oder mehrere dieser Werte fest, und die Clients interpretieren den Status entsprechend Ihrer Anwendung. Beispielsweise kann ein Client den Ordner Status verwenden, um zwischen Ordnern in einer Hierarchietabelle visuell zu unterscheiden, sodass Ordner mit demselben Status auf die gleiche Weise angezeigt werden. Hervorgehobene Ordner können in umgekehrtem Video angezeigt werden, markierte Ordner und zum Löschen markierte Ordner können mit einem sinnvollen Symbol angezeigt werden, und versteckte Ordner können verborgen werden.
  
Die Bits 16 bis 31 ("0x10000" bis "0x80000000") dieser Eigenschaft stehen für die IPM-Clientanwendung zur Verfügung. Alle anderen Bits sind für die Verwendung durch MAPI reserviert; diejenigen, die nicht in der obigen Liste definiert sind, sollten anfänglich auf NULL festgelegt und nicht geändert werden.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
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

