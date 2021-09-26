---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b90b6705909219acfe7337baedce105de301feb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610944"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zerstört eine [ADRLIST-Struktur](adrlist.md) und gibt den zugeordneten Speicher frei, einschließlich des Speichers, der für alle Memberarrays und -strukturen reserviert ist. 
  
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

 _Padrlist_
  
> [in] Zeiger auf die zu zerstörende **ADRLIST-Struktur.** 
    
## <a name="return-value"></a>Return value

None.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Rahmen der Implementierung von **FreePadrlist** ruft MAPI die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um jeden Eintrag in der **ADRLIST-Struktur** freizustellen, bevor die vollständige Struktur freigegeben wird. Daher müssen alle diese Einträge den Zuordnungsregeln für die [ADRLIST-Struktur](adrlist.md) gefolgt sein, wobei ein einzelner [MAPIAllocateBuffer-Aufruf](mapiallocatebuffer.md) für jedes Memberarray und jede Struktur verwendet wird. 
  
Weitere Informationen zum Zuordnen von Speicher für **ADRLIST-** und **SRowSet-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **FreePadrlist-Methode,** um eine ADRLIST-Struktur freizugeben, die erstellt wurde, um einer Nachricht eine einmalige Adresse hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

