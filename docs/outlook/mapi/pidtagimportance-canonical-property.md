---
title: Kanonische PidTagImportance-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d91720bc2e612345cff4221dbdd9c41a45b149e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587664"
---
# <a name="pidtagimportance-canonical-property"></a>Kanonische PidTagImportance-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der die Meinung des Absenders der Nachricht zur Wichtigkeit einer Nachricht angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IMPORTANCE  <br/> |
|Kennung:  <br/> |0x0017  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft und die **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) -Eigenschaft sollten nicht verwechselt werden. Wichtigkeit gibt den Benutzern einen Wert an, während die Priorität die Reihenfolge oder Geschwindigkeit angibt, in der die Nachricht von der Messagingsystemsoftware gesendet werden soll. Eine höhere Priorität weist in der Regel auf höhere Kosten hin. Eine höhere Wichtigkeit wird in der Regel einer anderen Anzeige über die Benutzeroberfläche zugeordnet. 
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
IMPORTANCE_LOW 
  
> Die Nachricht hat eine geringe Wichtigkeit.
    
IMPORTANCE_HIGH 
  
> Die Nachricht hat eine hohe Wichtigkeit.
    
IMPORTANCE_NORMAL 
  
> Die Nachricht hat normale Wichtigkeit.
    
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

