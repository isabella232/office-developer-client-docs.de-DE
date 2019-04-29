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
  
Zerstört eine [ADRLIST](adrlist.md) -Struktur und gibt zugeordneten Arbeitsspeicher frei, einschließlich des Arbeitsspeichers, der für alle Elementarrays und-Strukturen reserviert ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Parameter

 _padrlist_
  
> in Zeiger auf die **ADRLIST** -Struktur, die zerstört werden soll. 
    
## <a name="return-value"></a>Return value

None.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Rahmen der Implementierung von **FreePadrlist**ruft MAPI die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um jeden Eintrag in der **ADRLIST** -Struktur freizugeben, bevor die gesamte Struktur freigegeben wird. Daher müssen alle diese Einträge den Zuordnungsregeln für die [ADRLIST](adrlist.md) -Struktur unter Verwendung eines einzelnen [MAPIAllocateBuffer](mapiallocatebuffer.md) -Aufrufs für die einzelnen Elementarrays und-Strukturen gefolgt sein. 
  
Weitere Informationen zum Zuweisen von Arbeitsspeicher für **ADRLIST** -und **SRowSet** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **FreePadrlist** -Methode, um eine ADRLIST-Struktur freizugeben, die zum Hinzufügen einer einmaligen Adresse zu einer Nachricht erstellt wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

