---
title: PidTagConflictItems (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4703924e77c616fdc0ff47bf5b7b4a240ae1f1e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563763"
---
# <a name="pidtagconflictitems-canonical-property"></a>PidTagConflictItems (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine oder mehrere Eintrags-IDs von Elementen, die an einer automatischen Konfliktlösung beteiligt waren.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Kennung:  <br/> |0x1098  <br/> |
|Eigenschaftentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Zu den Standardtypen von Microsoft Outlook Elementen, die die automatische Konfliktlösung unterstützen, gehören die folgenden Standardelementtypen: Terminelemente, Kontaktelemente, Journalelemente, E-Mail-Elemente, Besprechungselemente, Kurznotizelemente und Aufgabenelemente. Ein Element, das zu einer Nachrichtenklasse gehört, die von einem dieser Standardelementtypen abgeleitet ist, unterstützt auch die automatische Konfliktlösung. In Microsoft Outlook 2003 und Microsoft Office Outlook 2007, wenn Outlook Elemente synchronisiert und der Ansicht ist, dass die resultierende Kopie möglicherweise nicht alle wichtigen Daten enthält, speichert Outlook die konflikteigen Kopien im Ordner **"Konflikte"** im Ordner **"Synchronisierungsprobleme".** 
  
> [!NOTE]
> **Synchronisierungsprobleme** und die zugehörigen Unterordner werden ausgeblendet, bis Sie im Menü **"Los"** auf **"Ordnerliste"** klicken. 
  
Ein Element macht die **PR_CONFLICT_ITEMS** Eigenschaft verfügbar, wenn es sich um einen der Elementtypen handelt, die die automatische Konfliktbehebung unterstützen, in einer Konfliktbehebung gewonnen oder aufgrund einer Konfliktbehebung in den Ordner **"Konflikte"** verschoben wurde. Der Ordner, in dem das Element abgelegt wird, bestimmt den Inhalt **PR_CONFLICT_ITEMS**. Wenn sich das Element in einem anderen Ordner als dem Ordner **"Konflikte"** befindet und das Element die **PR_CONFLICT_ITEMS** Eigenschaft verfügbar macht, muss das Element die Konfliktbehebung gewonnen haben, und **PR_CONFLICT_ITEMS** eine oder mehrere Eintrags-IDs dieser Elemente enthalten würde, die in der Konfliktbehebung verloren gegangen sind. Wenn sich das Element im Ordner **"Konflikte"** befindet und das Element die **PR_CONFLICT_ITEMS** Eigenschaft verfügbar macht, muss dieses Element die Konfliktbehebung verloren haben, und **PR_CONFLICT_ITEMS** würde die Eintrags-ID des Elements enthalten, das in der Konfliktbehebung gewonnen hat. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Nachrichtenobjektdaten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

