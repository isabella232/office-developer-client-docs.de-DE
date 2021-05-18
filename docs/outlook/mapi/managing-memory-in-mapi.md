---
title: Verwalten von Arbeitsspeicher in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298096"
---
# <a name="managing-memory-in-mapi"></a>Verwalten von Arbeitsspeicher in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Wissen, wie und wann Arbeitsspeicher zugewiesen und frei werden soll, ist ein wichtiger Bestandteil der Programmierung mit MAPI. MAPI stellt Funktionen und Makros zur Verfügung, die Ihr Client oder Dienstanbieter verwenden kann, um den Arbeitsspeicher konsistent zu verwalten. Die drei Funktionen sind wie folgt:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Wenn Clients und Dienstanbieter diese Funktionen verwenden, wird das Problem, wer "besitzt", d. h. weiß, wie sie freigegeben werden, beseitigt. Ein Client, der eine Dienstanbietermethode aufruft, muss keinen Puffer übergeben, der groß genug ist, um einen Rückgabewert beliebiger Größe zu halten. Der Dienstanbieter kann einfach mithilfe von **MAPIAllocateBuffer** und, falls erforderlich, **MAPIAllocateMore**, die entsprechende Menge an Arbeitsspeicher zuordnen, und der Client kann ihn später mithilfe von **MAPIFreeBuffer**, unabhängig vom Dienstanbieter, nach Besorgung veröffentlichen. 
  
Die Speichermakros werden verwendet, um Strukturen oder Arrays von Strukturen einer bestimmten Größe zuzuordnen. Clients und Dienstanbieter sollten diese Makros verwenden, anstatt den Arbeitsspeicher manuell zuzuordnen. Wenn ein Client beispielsweise eine Namensauflösungsverarbeitung für eine Empfängerliste mit drei Einträgen durchführen muss, kann das **Makro SizedADRLIST** verwendet werden, um eine **ADRLIST-Struktur** zu erstellen, die an **IAddrBook::ResolveName** mit der richtigen Anzahl von **ADRENTRY-Mitgliedern** übergeben wird. Alle Speichermakros sind in MAPIDEFS definiert. H-Headerdatei. Diese Makros sind: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI unterstützt auch die Verwendung der COM-Schnittstelle [IMalloc für die](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) Speicherverwaltung. Dienstanbieter erhalten zum Zeitpunkt der Initialisierung einen **IMalloc-Schnittstellenzeiger** von MAPI und können auch einen über die [MAPIGetDefaultMalloc-Funktion](mapigetdefaultmalloc.md) abrufen. Der Hauptvorteil bei der Verwendung der **IMalloc-Methoden** zum Verwalten von Arbeitsspeicher über die MAPI-Funktionen besteht in der Möglichkeit, mit den COM-Methoden einen vorhandenen Puffer neu zu ordnen. Die MAPI-Speicherfunktionen unterstützen keine Neuzuordnung. 
  

