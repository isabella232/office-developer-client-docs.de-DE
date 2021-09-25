---
title: Verwalten des Arbeitsspeichers in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19a91c02bfb5ba3cd446643ac7039841f17d1a05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571514"
---
# <a name="managing-memory-in-mapi"></a>Verwalten des Arbeitsspeichers in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zu wissen, wie und wann Speicher zugeordnet und freigegeben werden soll, ist ein wichtiger Bestandteil der Programmierung mit MAPI. MAPI stellt Funktionen und Makros bereit, die Ihr Client oder Dienstanbieter verwenden kann, um den Speicher konsistent zu verwalten. Die drei Funktionen sind wie folgt:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Wenn Clients und Dienstanbieter diese Funktionen verwenden, wird das Problem, wem "gehört" – d. h. wie sie freigegeben werden sollen – ein bestimmter Speicherblock eliminiert. Ein Client, der eine Dienstanbietermethode aufruft, muss keinen Puffer übergeben, der groß genug ist, um einen Rückgabewert beliebiger Größe zu speichern. Der Dienstanbieter kann einfach die entsprechende Menge an Arbeitsspeicher mit **MAPIAllocateBuffer** und, falls erforderlich, **MAPIAllocateMore** zuordnen, und der Client kann ihn später mit **MAPIFreeBuffer** unabhängig vom Dienstanbieter freigeben. 
  
Die Speichermakros werden verwendet, um Strukturen oder Arrays von Strukturen einer bestimmten Größe zuzuweisen. Clients und Dienstanbieter sollten diese Makros verwenden, anstatt den Speicher manuell zuzuweisen. Wenn ein Client beispielsweise eine Namensauflösungsverarbeitung für eine Empfängerliste mit drei Einträgen durchführen muss, kann das **Makro SizeADRLIST** verwendet werden, um eine **ADRLIST-Struktur** zu erstellen, die an **IAddrBook::ResolveName** mit der richtigen Anzahl von **ADRENTRY-Membern** übergeben wird. Alle Speichermakros werden in MAPIDEFS definiert. H-Headerdatei. Diese Makros sind: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI unterstützt auch die Verwendung der COM-Schnittstelle [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) für die Speicherverwaltung. Dienstanbieter erhalten einen **IMalloc-Schnittstellenzeiger** von MAPI zur Initialisierungszeit und können einen auch über die [MAPIGetDefaultMalloc-Funktion](mapigetdefaultmalloc.md) abrufen. Der Hauptvorteil der Verwendung der **IMalloc-Methoden** für die Verwaltung des Arbeitsspeichers über die MAPI-Funktionen besteht darin, dass es mit den COM-Methoden möglich ist, einen vorhandenen Puffer neu zuzuordnen. Die MAPI-Speicherfunktionen unterstützen keine Neuzuordnung. 
  

