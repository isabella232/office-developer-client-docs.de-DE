---
title: PidTagConflictItems (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338017"
---
# <a name="pidtagconflictitems-canonical-property"></a>PidTagConflictItems (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine oder mehrere Eintrags-IDs von Elementen, die an einer automatischen Konfliktlösung beteiligt waren.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Kennung:  <br/> |0x1098  <br/> |
|Eigenschaftstyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Typen von standardmäßigen Microsoft Outlook-Elementen, die die automatische Konfliktlösung unterstützen, umfassen die folgenden Standardelementtypen: Terminelemente, Kontaktelemente, Journalelemente, E-Mail-Elemente, Besprechungselemente, Notizelemente und Aufgabenelemente. Ein Element einer Nachrichtenklasse, das von einem dieser Standardelementtypen ab leitet, unterstützt auch die automatische Konfliktlösung. Wenn Outlook in Microsoft Outlook 2003 und Microsoft Office Outlook 2007 Elemente synchronisiert und der Ansicht ist, dass die sich ausdingende Kopie möglicherweise nicht alle wichtigen  Daten enthält,  speichert Outlook die in Konflikt konfliktenden Kopien im Ordner Konflikte unter dem Ordner Synchronisierungsprobleme. 
  
> [!NOTE]
> **Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu. 
  
Ein Element macht die **PR_CONFLICT_ITEMS-Eigenschaft** verfügbar, wenn es sich um einen der Elementtypen handelt, die die  automatische Konfliktlösung unterstützen, in einer Konfliktlösung gewonnen haben oder aufgrund einer Konfliktauflösung im Ordner Konflikte platziert wurden. Der Ordner, in dem das Element platziert wird, bestimmt den Inhalt **PR_CONFLICT_ITEMS.** Wenn sich das Element in einem  anderen Ordner als dem Ordner Konflikte befindet und das Element die **PR_CONFLICT_ITEMS-Eigenschaft** verfügbar macht, muss das Element die Konfliktauflösung gewonnen haben, und **PR_CONFLICT_ITEMS** würde eine oder mehrere Eintrags-IDs dieser Elemente enthalten, die in der Konfliktlösung verloren gegangen sind. Wenn sich das Element  im Ordner Konflikte befindet und das Element die **PR_CONFLICT_ITEMS-Eigenschaft** verfügbar macht, muss dieses Element die Konfliktauflösung verloren haben, und **PR_CONFLICT_ITEMS** würde die Eintrags-ID des Elements enthalten, das in der Konfliktauflösung gewonnen wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

