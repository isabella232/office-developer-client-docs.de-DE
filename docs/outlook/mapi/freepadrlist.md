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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2c5d4ec8381d6614cc2bc92fb0a762b068a97a81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791755"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Betrifft**: Outlook 
  
Löscht eine [ADRLIST](adrlist.md) -Struktur und zugehörige Speicher, einschließlich des Speichers für alle Member Arrays und Strukturen frei. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Parameter

 _padrlist_
  
> [in] Zeiger auf die **ADRLIST** -Struktur, die gelöscht werden. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Als Teil der Implementierung der **FreePadrlist**ruft MAPI die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um alle Einträge in der Struktur **ADRLIST** frei, bevor die vollständige Struktur freigegeben. Daher müssen alle diese Einträge die Zuweisung Regeln für die [ADRLIST](adrlist.md) -Struktur befolgt haben, mit einer einzelnen [MAPIAllocateBuffer](mapiallocatebuffer.md) rufen Sie für jedes Array mit Mitgliedern und Struktur. 
  
Weitere Informationen zum Zuweisen von Arbeitsspeicher für **ADRLIST** und **SRowSet** Strukturen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI (engl.) verwendet die **FreePadrlist** -Methode, um eine ADRLIST-Struktur frei, die zum Hinzufügen einer einmaligen Adresse auf eine Nachricht erstellt wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

