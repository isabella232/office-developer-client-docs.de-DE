---
title: Verwalten von Speicher für ADRLIST- und SRowSet-Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad3a05a2556512ad06ab52abda29d4bb66fbd605
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561278"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Verwalten des Speichers für ADRLIST- und SRowSet-Strukturen"

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Anforderung, nach Möglichkeit den gesamten Speicher für einen Puffer mit einem einzelnen **MAPIAllocateBuffer-Aufruf** zuzuweisen, gilt nicht bei Verwendung der Adressliste oder **ADRLIST-** und Zeilensatz- oder **SRowSet-Strukturen.** 
  
Diese beiden Strukturen sind Ausnahmen von den Standardregeln für die Zuweisung und Freigabe von Arbeitsspeicher. Sie enthalten mehrere Ebenen von Strukturen und sind so konzipiert, dass einzelne Member hinzugefügt oder entfernt werden können. Daher muss jede Eigenschaft eine separate Zuordnung sein. 

Wenn die meisten Strukturen mit einem Aufruf von **MAPIFreeBuffer** freigegeben werden, muss jeder einzelne Eintrag in einer **ADRLIST-** oder **SRowSet-Struktur** mit einem eigenen Aufruf von **MAPIFreeBuffer** oder einem einzigen Aufruf von **FreeProws** oder **FreePadrlist** freigegeben werden. Weitere Informationen finden Sie unter [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)und [SRowSet](srowset.md). 

**FreeProws** und **FreePadrlist** sind Funktionen, die von MAPI bereitgestellt werden, um die Freigabe dieser Datenstrukturen zu vereinfachen. Weitere Informationen finden Sie unter ["FreeProws"](freeprows.md) und ["FreePadrlist".](freepadrlist.md) **FreePadrlist** gibt den Speicher für die **ADRLIST-Struktur** sowie den gesamten zugeordneten Speicher für die Strukturmember frei. **FreeProws** führt dieselbe Vorgehensweise für die **SRowSet-Struktur** aus. 
  
Das folgende Diagramm zeigt das Layout einer **ADRLIST-Datenstruktur,** das die erforderlichen separaten Speicherzuweisungen angibt. Die grauen Felder zeigen Speicher an, der mit einem Einzigen Anruf zugeordnet und freigegeben werden kann. 
  
**ADRLIST-Speicherzuweisung**
  
![ADRLIST-Speicherzuweisung](media/amapi_52.gif "ADRLIST-Speicherzuweisung")
  
## <a name="see-also"></a>Siehe auch

- [Verwalten des Arbeitsspeichers in MAPI](managing-memory-in-mapi.md)

