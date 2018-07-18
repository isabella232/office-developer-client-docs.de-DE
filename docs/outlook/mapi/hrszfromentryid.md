---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791937"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Betrifft**: Outlook 
  
Eine Eintrags-ID codiert in eine ASCII-Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Parameter

 _cb_
  
> [in] Größe des Eintrags-ID, die auf das durch den Parameter _Pentry_ in Bytes. 
    
 _pentry_
  
> [in] Zeiger auf eine [ENTRYID](entryid.md) -Struktur, die Eintrags-ID zu codierenden enthält. 
    
 _psz_
  
> [out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge.
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Bemerkungen

Die Funktionen [HrEntryIDFromSz](hrentryidfromsz.md) und **HrSzFromEntryID** bieten eine Konvertierung zwischen der Zeichenfolge und der binären Formate der Eintragsbezeichner. Mit MAPI sollten Sie die Strukturen mit Binärdaten verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrSzFromEntryID** -Funktion weist Speicher für die Verwendung der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) ASCII-Zeichenfolge. 
  

