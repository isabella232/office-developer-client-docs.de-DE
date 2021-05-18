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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407865"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Verwalten des Arbeitsspeichers für ADRLIST- und SRowSet-Strukturen"

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Anforderung, bei einem einzelnen **MAPIAllocateBuffer-Aufruf** nach Möglichkeit allen Arbeitsspeicher für einen Puffer zuzuordnen, gilt nicht, wenn die Adressliste oder **ADRLIST** und zeilensatz- oder **SRowSet**-Strukturen verwendet werden. 
  
Diese beiden Strukturen sind Ausnahmen von den Standardregeln für die Zuweisung und Freigabe von Arbeitsspeicher. Sie enthalten mehrere Ebenen von Strukturen und sollen das Hinzufügen oder Entfernen einzelner Elemente ermöglichen. Daher muss jede Eigenschaft eine separate Zuordnung sein. 

Wenn die meisten Strukturen mit einem Aufruf von **MAPIFreeBuffer** frei werden, muss jeder einzelne Eintrag in einer **ADRLIST-** oder **SRowSet-Struktur** mit einem eigenen Aufruf von **MAPIFreeBuffer** oder einem einzelnen Aufruf von **FreeProws** oder **FreePadrlist** frei werden. Weitere Informationen finden Sie unter [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)und [SRowSet](srowset.md). 

**FreeProws** und **FreePadrlist** sind Funktionen, die von MAPI bereitgestellt werden, um das Freispeichern dieser Datenstrukturen zu vereinfachen. Weitere Informationen finden Sie unter [FreeProws](freeprows.md) und [FreePadrlist](freepadrlist.md). **FreePadrlist** gibt den Arbeitsspeicher für die **ADRLIST-Struktur** sowie den zugeordneten Arbeitsspeicher für die Strukturmitglieder frei. **FreeProws** führt dasselbe für die **SRowSet-Struktur** aus. 
  
Das folgende Diagramm zeigt das Layout einer **ADRLIST-Datenstruktur,** die die erforderlichen separaten Speicherzuweisungen angibt. In den grauen Feldern wird der Speicher angezeigt, der mit einem Aufruf zugewiesen und freigegeben werden kann. 
  
**ADRLIST-Speicherzuweisung**
  
![ADRLIST-Speicherzuweisung](media/amapi_52.gif "ADRLIST-Speicherzuweisung")
  
## <a name="see-also"></a>Siehe auch

- [Verwalten von Arbeitsspeicher in MAPI](managing-memory-in-mapi.md)

