---
title: Kanonische PidTagImportance-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327923"
---
# <a name="pidtagimportance-canonical-property"></a>Kanonische PidTagImportance-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der die Meinung des Nachrichtenabsenders zur Wichtigkeit einer Nachricht angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IMPORTANCE  <br/> |
|Kennung:  <br/> |0x0017  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft und die **PR_PRIORITY** ([pidtagpriority (](pidtagpriority-canonical-property.md))-Eigenschaft sollten nicht verwechselt werden. Wichtigkeit gibt einen Wert für Benutzer an, während Priority die Reihenfolge oder Geschwindigkeit angibt, mit der die Nachricht von der Messagingsystem Software gesendet werden soll. Höhere Priorität weist in der Regel auf höhere Kosten hin. Höhere Wichtigkeit wird in der Regel einer anderen Anzeige von der Benutzeroberfläche zugeordnet. 
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
IMPORTANCE_LOW 
  
> Die Nachricht hat eine geringe Wichtigkeit.
    
IMPORTANCE_HIGH 
  
> Die Nachricht hat eine hohe Wichtigkeit.
    
IMPORTANCE_NORMAL 
  
> Die Nachricht hat eine normale Wichtigkeit.
    
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

