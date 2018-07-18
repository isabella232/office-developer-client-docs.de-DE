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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 61176ec6f9ff00fa5a38a2b385cb5281fa40961e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794166"
---
# <a name="pidtagconflictitems-canonical-property"></a>PidTagConflictItems (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine oder mehrere Eintrags-IDs der Elemente, die in einer automatischen Konfliktbehebung beteiligt waren.
  
## 

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Bezeichner:  <br/> |0x1098  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Typen von standard Microsoft Outlook-Elementen, die automatische Konfliktbehebung unterstützen die folgenden standardmäßigen Elementtypen enthalten: Terminelemente, Kontaktelementen, Journalelemente, e-Mail-Elementen, Elemente der Besprechung, Kurznotiz Elemente und Aufgabenelementen. Ein Element zu einer Nachrichtenklasse, die auch von einer der folgenden standardmäßigen Elementtypen abgeleitet ist gehören unterstützt automatische Konfliktbehebung. In Microsoft Outlook 2003 und Microsoft Office Outlook 2007 Wenn Outlook Elemente synchronisiert und Auffassung besteht die Möglichkeit, dass die resultierende Kopie möglicherweise keine alle wichtige Daten enthalten, speichert Outlook die miteinander in Konflikt stehende Kopien in der **Konflikte** Ordner unterhalb des Ordners **Synchronisierungsprobleme** . 
  
> [!NOTE]
> **Synchronisierungsprobleme** und den zugehörigen Unterordnern sind ausgeblendet, bis Sie im Menü **Gehe zu** auf **Ordnerliste** klicken. 
  
Ein Element wird die **PR_CONFLICT_ITEMS** -Eigenschaft verfügbar gemacht, wenn gehört zu den Elementtypen, die automatische Konfliktbehebung unterstützen, einen Konfliktbehebung gewonnen hat oder wurde im Ordner **Konflikte** aufgrund einer Konfliktbehebung platziert. Der Ordner, in dem das Element verschoben wird, bestimmt den Inhalt der **PR_CONFLICT_ITEMS**. Wenn das Element sich im einige Ordner als dem Ordner **Konflikte befindet** und das Element die **PR_CONFLICT_ITEMS** -Eigenschaft macht, der Artikel muss die Konfliktbehebung erworben haben und **PR_CONFLICT_ITEMS** würde eine oder mehrere EntryIDs von Diese Elemente, die in der Konfliktbehebung verloren. Wenn das Element sich im Ordner **Konflikte befindet** und das Element wird die **PR_CONFLICT_ITEMS** -Eigenschaft verfügbar gemacht, dieses Element muss die Konfliktbehebung verloren haben und **PR_CONFLICT_ITEMS** würde die Eintrags-ID des Elements, das in den Konflikt gewonnen Auflösung. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

