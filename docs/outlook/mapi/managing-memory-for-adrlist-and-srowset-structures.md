---
title: Verwalten des Arbeitsspeichers für ADRLIST und SRowSet Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589728"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Verwalten des Arbeitsspeichers für ADRLIST und SRowSet Strukturen"

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Anforderung für einen Puffer mit einem einzigen Aufruf **MAPIAllocateBuffer** möglichst alle Speicher wird bei Verwendung der Adressliste oder **ADRLIST**, und die Zeile Set oder **SRowSet**, Strukturen nicht angewendet. 
  
Diese zwei Strukturen sind Ausnahmen für die standard-Regeln für das zuordnen und Freigeben von Arbeitsspeicher. Enthalten mehrere Ebenen von Strukturen, und aktivieren einzelne Mitglieder hinzugefügt oder entfernt werden sollen. Aus diesem Grund muss jede Eigenschaft eine separate Zuordnung. 

Wobei die meisten Strukturen mit einem einzigen Aufruf **MAPIFreeBuffer**, jeden einzelnen Eintrag in einer **ADRLIST** oder **SRowSet** freigegeben werden, muss mit einem eigenen Aufruf **MAPIFreeBuffer** oder einem einzigen Aufruf von **FreeProws** oder **freigegeben werden FreePadrlist**. Weitere Informationen finden Sie unter [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)und [SRowSet](srowset.md). 

**FreeProws** und **FreePadrlist** sind Funktionen zur Vereinfachung der die Freigabe dieser Datenstrukturen MAPI bereitgestellt. Weitere Informationen finden Sie unter [FreeProws](freeprows.md) und [FreePadrlist](freepadrlist.md). **FreePadrlist** frei der Arbeitsspeicher für die **ADRLIST** -Struktur sowie alle zugehörigen Speicher für die Struktur Mitglieder; **FreeProws** führt den gleichen Wert für die **SRowSet** -Struktur. 
  
Das folgende Diagramm zeigt das Layout der **ADRLIST** -Datenstruktur, der angibt, der separate Arbeitsspeicher Zuweisungen erforderlich. Die grauen Felder anzeigen Arbeitsspeicher, die reserviert und mit einem einzigen Aufruf freigegeben werden kann. 
  
**ADRLIST-Speicherzuweisung**
  
![ADRLIST-speicherzuweisung] (media/amapi_52.gif "ADRLIST-speicherzuweisung")
  
## <a name="see-also"></a>Siehe auch

- [Verwalten von Arbeitsspeicher in MAPI](managing-memory-in-mapi.md)

