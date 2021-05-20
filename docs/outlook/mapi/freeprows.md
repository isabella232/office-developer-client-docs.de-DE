---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438820"
---
# <a name="freeprows"></a>FreeProws

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zerstört eine [SRowSet-Struktur](srowset.md) und gibt den zugeordneten Arbeitsspeicher frei, einschließlich des für alle Memberarrays und -strukturen zugewiesenen Arbeitsspeichers. 
  
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

 _prows_
  
> [in] Zeiger auf die **zu zerstörende SRowSet-Struktur.** 
    
## <a name="return-value"></a>Return value

None.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Rahmen der Implementierung von **FreeProws** ruft MAPI die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um jeden Eintrag in der **SRowSet-Struktur** frei zu geben, bevor die vollständige Struktur frei wird. Daher müssen alle diese Einträge die Zuweisungsregeln für die [SRowSet-Struktur](srowset.md) befolgt haben, indem sie einen individuellen [MAPIAllocateBuffer-Aufruf](mapiallocatebuffer.md) für jedes Elementarray und jede Elementstruktur verwenden. 
  
Weitere Informationen zum Zuordnen von Arbeitsspeicher für **ADRLIST-** und **SRowSet-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **FreeProws-Methode,** um eine SRowSet-Struktur frei zu geben, die Zeilen der zu verarbeitenden Tabelle enthält.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

