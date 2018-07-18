---
title: PidLidAutoProcessState (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793445"
---
# <a name="pidlidautoprocessstate-canonical-property"></a>PidLidAutoProcessState (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt die Optionen an, mit denen auf die automatische Verarbeitung von e-Mail-Nachrichten.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidSniffState  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000851A  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Eigenschaft nicht vorhanden ist, möglicherweise in diesem Fall ist der Standardwert der "0 x 00000000" verwendet. Wenn Sie festlegen möchten, muss diese Eigenschaft auf einen der Werte in der folgenden Tabelle festgelegt werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Verarbeiten Sie die Nachricht nicht automatisch.  <br/> |
|0x00000001  <br/> |Die Nachricht automatisch verarbeiten, oder wenn die Nachricht geöffnet wird.  <br/> |
|0x00000002  <br/> |Verarbeitet die Nachricht nur, wenn die Nachricht geöffnet wird.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

