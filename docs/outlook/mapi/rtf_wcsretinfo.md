---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 65d3758cc0abe8835c43887558cdd9f60aeaca85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609607"
---
# <a name="rtf_wcsretinfo"></a>RTF_WCSRETINFO

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Struktur enthält Informationen zu einem Stream im systemeigenen Format, der durch dekomprimieren des Textkörpers einer Nachricht zurückgegeben wird, die im komprimierten RtF (Rich Text Format) gekapselt ist.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Elemente

_size_
  
> Die Größe der **RTF_WCSRETINFO** Struktur in der Anzahl der Bytes. 
    
_ulStreamFlags_
  
> Dies ist ein Wert, der das Format des systemeigenen Textkörpers angibt. Dieser Wert ist nur gültig, wenn das **MAPI_NATIVE_BODY** Flag im  _ulFlags-Parameter_ der [RTF_WCSINFO](rtf_wcsinfo.md) Struktur übergeben wird, die an die [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) übergeben wird. Dies kann einer der folgenden Werte sein: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Dieser Wert wird nur verwendet, wenn  _ulFlags_ das **flag MAPI_NATIVE_BODY** enthält und der Textkörper RTF ist.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Dieser Wert wird nur verwendet, wenn  _ulFlags_ das **flag MAPI_NATIVE_BODY** enthält und der Textkörper nur ein Textformat aufweist.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Dieser Wert wird nur verwendet, wenn  _ulFlags_ das **flag MAPI_NATIVE_BODY** enthält und der Textkörper das HTML-Format (Hypertext Markup Language) aufweist.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

