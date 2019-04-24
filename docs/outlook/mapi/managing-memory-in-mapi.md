---
title: Verwalten von Speicher in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298096"
---
# <a name="managing-memory-in-mapi"></a>Verwalten von Speicher in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zu wissen, wie und wann Speicher reserviert und freigegeben werden muss, ist ein wichtiger Teil der Programmierung mit MAPI. MAPI bietet sowohl Funktionen als auch Makros, die der Client oder Dienstanbieter zur konsistenten Verwaltung des Arbeitsspeichers verwenden kann. Die drei Funktionen lauten wie folgt:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Wenn Clients und Dienstanbieter diese Funktionen verwenden, wird das Problem der WHO "besitzt", d. h., die Veröffentlichung eines bestimmten Speicherblocks verhindert. Ein Client, der eine Dienstanbieter Methode aufruft, muss keinen Puffer übergeben, der groß genug ist, um einen Rückgabewert beliebiger Größe aufzunehmen. Der Dienstanbieter kann einfach die entsprechende Menge an Arbeitsspeicher mithilfe von **MAPIAllocateBuffer** und, falls erforderlich, **MAPIAllocateMore**, und der Client kann ihn später unter Verwendung von **mapifreebufferfreigegeben**unabhängig vom Dienst freigeben. Anbieter. 
  
Die Speicher Makros werden verwendet, um Strukturen oder Arrays von Strukturen mit einer bestimmten Größe zuzuweisen. Clients und Dienstanbieter sollten diese Makros anstelle des Arbeitsspeichers manuell verwenden. Wenn beispielsweise ein Client die Verarbeitung von Namensauflösung für eine Empfängerliste mit drei Einträgen durchführen muss, kann das **SizedADRLIST** -Makro verwendet werden, um eine **ADRLIST** -Struktur zu erstellen, die an **IAddrBook::** ResolveName mit der richtigen Anzahl von **Miet** Mitglieder. Alle Arbeitsspeicher Makros werden in der MAPIDEFS definiert. H-Headerdatei. Diese Makros sind: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI unterstützt auch die Verwendung der COM- [](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) Schnittstelle IMalloc für die Speicherverwaltung. Dienstanbieter erhalten einen **IMalloc** -Schnittstellenzeiger von MAPI zur Initialisierungszeit und können auch einen über die [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) -Funktion abrufen. Der Hauptvorteil bei der Verwendung **** der IMalloc-Methoden zum Verwalten des Speichers über die MAPI-Funktionen besteht darin, dass mit den com-Methoden ein vorhandener Puffer neu zugewiesen werden kann. Die MAPI-Speicherfunktionen unterstützen die Neuzuordnung nicht. 
  

