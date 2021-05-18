---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408642"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zerstört eine [ADRLIST-Struktur](adrlist.md) und gibt den zugeordneten Arbeitsspeicher frei, einschließlich des für alle Memberarrays und -strukturen zugewiesenen Arbeitsspeichers. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Parameter

 _padrlist_
  
> [in] Zeiger auf die zu zerstörende **ADRLIST-Struktur.** 
    
## <a name="return-value"></a>Return value

None.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Rahmen der Implementierung von **FreePadrlist** ruft MAPI die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um jeden Eintrag in der **ADRLIST-Struktur** frei zu geben, bevor die vollständige Struktur frei wird. Daher müssen alle diese Einträge die Zuweisungsregeln für die [ADRLIST-Struktur](adrlist.md) befolgt haben, indem sie einen individuellen [MAPIAllocateBuffer-Aufruf](mapiallocatebuffer.md) für jedes Elementarray und jede Elementstruktur verwenden. 
  
Weitere Informationen zum Zuordnen von Arbeitsspeicher für **ADRLIST-** und **SRowSet-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **FreePadrlist-Methode,** um eine ADRLIST-Struktur frei zu geben, die zum Hinzufügen einer einmal verwendeten Adresse zu einer Nachricht erstellt wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

