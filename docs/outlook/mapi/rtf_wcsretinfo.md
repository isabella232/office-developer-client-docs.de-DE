---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426170"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Struktur stellt Informationen zu einem Stream im systemeigenen Format bereit, der von der Dekomprimierung des Texts einer Nachricht zurückgegeben wird, die im komprimierten Rich-Text-Format (RTF) gekapselt ist.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Elemente

_size_
  
> Die Größe der **RTF_WCSRETINFO** -Struktur in der Anzahl von Bytes. 
    
_ulStreamFlags_
  
> Dies ist ein Wert, der das Format des systemeigenen Texts angibt. Dieser Wert ist nur gültig, wenn das **MAPI_NATIVE_BODY** -Flag im _ulFlags_ -Parameter der [RTF_WCSINFO](rtf_wcsinfo.md) -Struktur übergeben wird, die an die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion übergeben wird. Dabei kann es sich um einen der folgenden Werte handeln: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Dieser Wert wird nur verwendet, wenn _ulFlags_ das **MAPI_NATIVE_BODY** -Flag enthält und der Text RTF ist.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Dieser Wert wird nur verwendet, wenn _ulFlags_ das **MAPI_NATIVE_BODY** -Flag enthält und der Text nur-Text-Format aufweist.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Dieser Wert wird nur verwendet, wenn _ulFlags_ das **MAPI_NATIVE_BODY** -Flag enthält, und der Text im HTML-Format (Hypertext Markup Language).  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

