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
  
Zerstört eine [SRowSet](srowset.md) -Struktur und gibt zugeordneten Arbeitsspeicher frei, einschließlich des Arbeitsspeichers, der für alle Elementarrays und-Strukturen reserviert ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Parameter

 _PROWS_
  
> in Zeiger auf die **SRowSet** -Struktur, die zerstört werden soll. 
    
## <a name="return-value"></a>Return value

None.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Rahmen der Implementierung von **FreeProws**ruft MAPI die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um jeden Eintrag in der **SRowSet** -Struktur freizugeben, bevor die gesamte Struktur freigegeben wird. Daher müssen alle diese Einträge den Zuordnungsregeln für die [SRowSet](srowset.md) -Struktur unter Verwendung eines einzelnen [MAPIAllocateBuffer](mapiallocatebuffer.md) -Aufrufs für die einzelnen Elementarrays und-Strukturen gefolgt sein. 
  
Weitere Informationen zum Zuweisen von Arbeitsspeicher für **ADRLIST** -und **SRowSet** -Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI verwendet die **FreeProws** -Methode, um eine SRowSet-Struktur mit Zeilen der verarbeiteten Tabelle freizugeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

