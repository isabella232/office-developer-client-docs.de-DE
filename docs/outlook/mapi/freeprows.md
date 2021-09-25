---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a71322552b12e806242ffcf78346f1f6d0b3e08b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561782"
---
# <a name="freeprows"></a>FreeProws

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zerstört eine [SRowSet-Struktur](srowset.md) und gibt den zugeordneten Speicher frei, einschließlich des Speichers, der für alle Memberarrays und -strukturen reserviert ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Parameter

 _Prows_
  
> [in] Zeiger auf die zu zerstörende **SRowSet-Struktur.** 
    
## <a name="return-value"></a>Return value

None.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Rahmen der Implementierung von **FreeProws** ruft MAPI die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um jeden Eintrag in der **SRowSet-Struktur** frei zu geben, bevor die vollständige Struktur freigegeben wird. Daher müssen alle diese Einträge den Zuordnungsregeln für die [SRowSet-Struktur](srowset.md) gefolgt sein, wobei ein einzelner [MAPIAllocateBuffer-Aufruf](mapiallocatebuffer.md) für jedes Memberarray und jede Elementstruktur verwendet wird. 
  
Weitere Informationen zum Zuordnen von Speicher für **ADRLIST-** und **SRowSet-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |AdrianThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **FreeProws-Methode,** um eine SRowSet-Struktur frei zu geben, die Zeilen der zu verarbeitenden Tabelle enthält.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

