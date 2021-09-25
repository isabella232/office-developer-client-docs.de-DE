---
title: Kanonische PidLidAutoProcessState-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 407a3ef2c40f190714ce3577a39242d0f7664d7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567039"
---
# <a name="pidlidautoprocessstate-canonical-property"></a>Kanonische PidLidAutoProcessState-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Optionen an, die bei der automatischen Verarbeitung von E-Mail-Nachrichten verwendet werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSniffState  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x0000851A  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Eigenschaft ist möglicherweise nicht vorhanden, in diesem Fall wird der Standardwert "0x00000000" verwendet. Wenn diese Eigenschaft festgelegt ist, muss sie auf einen der Werte in der folgenden Tabelle festgelegt werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Verarbeiten Sie die Nachricht nicht automatisch.  <br/> |
|0x00000001  <br/> |Verarbeiten Sie die Nachricht automatisch oder beim Öffnen der Nachricht.  <br/> |
|0x00000002  <br/> |Verarbeiten Sie die Nachricht nur, wenn die Nachricht geöffnet wird.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

