---
title: Verwalten von Speicher für ADRLIST- und SRowSet-Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298128"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Verwalten von Speicher für ADRLIST-und SRowSet-Strukturen "

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Anforderung zum Zuweisen des gesamten Speichers für einen Puffer, wann immer möglich mit einem einzelnen **MAPIAllocateBuffer** -Aufruf gilt nicht bei der Verwendung der Adressliste oder **ADRLIST**-und Zeilensatz-oder **SRowSet**-Strukturen. 
  
Diese beiden Strukturen sind Ausnahmen für die Standardregeln für das zuordnen und Freigeben von Arbeitsspeicher. Sie enthalten mehrere Ebenen von Strukturen und sollen das Hinzufügen oder Entfernen einzelner Elemente ermöglichen. Daher muss jede Eigenschaft eine separate Zuordnung sein. 

Wo die meisten Strukturen mit einem Aufruf von **mapifreebufferfreigegeben**freigegeben werden, muss jeder einzelne Eintrag in einer **ADRLIST** -oder **SRowSet** -Struktur mit einem eigenen Aufruf von **mapifreebufferfreigegeben** oder einem einzelnen Aufruf von **FreeProws** oder ** FreePadrlist**. Weitere Informationen finden Sie unter [mapifreebufferfreigegeben](mapifreebuffer.md), [ADRLIST](adrlist.md)und [SRowSet](srowset.md). 

**FreeProws** und **FREEPADRLIST** sind von MAPI bereitgestellte Funktionen zur Vereinfachung der Freigabe dieser Datenstrukturen. Weitere Informationen finden Sie unter [FreeProws](freeprows.md) und [FreePadrlist](freepadrlist.md). **FreePadrlist** gibt den Arbeitsspeicher für die **ADRLIST** -Struktur und den gesamten zugeordneten Arbeitsspeicher für die Strukturmember frei. **FreeProws** führt dasselbe für die **SRowSet** -Struktur aus. 
  
Das folgende Diagramm zeigt das Layout einer **ADRLIST** -Datenstruktur, die die getrennten Speicherzuordnungen angibt, die erforderlich sind. Die grauen Felder zeigen Arbeitsspeicher, der mit einem Anruf reserviert und freigegeben werden kann. 
  
**ADRLIST-Speicherzuweisung**
  
![ADRLIST-Speicherbelegung] (media/amapi_52.gif "ADRLIST-Speicherbelegung")
  
## <a name="see-also"></a>Siehe auch

- [Verwalten von Speicher in MAPI](managing-memory-in-mapi.md)

