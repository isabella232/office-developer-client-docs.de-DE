---
title: Kanonische Pidtagconflictitems (-Eigenschaft
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
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338017"
---
# <a name="pidtagconflictitems-canonical-property"></a>Kanonische Pidtagconflictitems (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine oder mehrere Eintrags-IDs von Elementen, die an einer automatischen Konfliktbehebung beteiligt waren.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Kennung:  <br/> |0x1098  <br/> |
|Eigenschafts:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Typen von standardmäßigen Microsoft Outlook-Elementen, die die automatische Konfliktbehebung unterstützen, sind die folgenden Standardelementtypen: Termin Elemente, Kontaktelemente, Journalelemente, e-Mail-Elemente, Besprechungselemente, Kurznotiz-Elemente und Aufgabenelemente. Ein Element, das zu einer Nachrichtenklasse gehört, die von einem dieser Standardelementtypen abgeleitet wird, unterstützt auch die automatische Konfliktbehebung. In Microsoft Outlook 2003 und Microsoft Office Outlook 2007 bei der Synchronisierung von Outlook-Elementen und der Ansicht, dass die resultierende Kopie nicht alle wesentlichen Daten enthalten kann, speichert Outlook die Konflikt verursachenden Kopien in den **Konflikten** . Ordner unter dem Ordner **Synchronisierungsprobleme** . 
  
> [!NOTE]
> **Synchronisierungsprobleme** und die zugehörigen Unterordner werden ausgeblendet, bis Sie im Menü **Gehe** zu auf **Ordnerliste** klicken. 
  
Ein Element macht die **PR_CONFLICT_ITEMS** -Eigenschaft verfügbar, wenn es sich um einen der Elementtypen handelt, die eine automatische Konfliktbehebung unterstützen, die in einer Konfliktlösung gewonnen wurde oder aufgrund einer Konfliktlösung im **Konflikt** Ordner abgelegt wurde. Der Ordner, in dem das Element abgelegt wird, bestimmt den Inhalt von **PR_CONFLICT_ITEMS**. Wenn sich das Element in einem anderen Ordner als dem Ordner " **Konflikte** " befindet und das Element die **PR_CONFLICT_ITEMS** -Eigenschaft verfügbar macht, muss das Element die Konfliktauflösung gewonnen haben, und **PR_CONFLICT_ITEMS** würde eine oder mehrere Eintrags-IDs enthalten. die Elemente, die bei der Konfliktlösung verloren gegangen sind. Wenn sich das Element im Ordner **Konflikte** befindet und das Element die **PR_CONFLICT_ITEMS** -Eigenschaft verfügbar macht, muss dieses Element die Konfliktauflösung verloren haben, und **PR_CONFLICT_ITEMS** würde die Eintrags-ID des Elements enthalten, das den Konflikt gewonnen hat. Lösung. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt das Synchronisieren von Messagingobjekt Daten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

