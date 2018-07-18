---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795411"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Betrifft**: Outlook 
  
Diese Struktur enthält Informationen zu einem Datenstrom im systemeigenen Format von Dekomprimieren den Textkörper einer Nachricht, die in der komprimierten Rich Text Format (RTF) zusammengefasst wird zurückgegeben.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Elemente

_Größe_
  
> Die Größe der Struktur **RTF_WCSRETINFO** als Byteanzahl angegeben. 
    
_ulStreamFlags_
  
> Dies ist ein Wert, der das Format des Textkörpers systemeigene angibt. Dieser Wert ist nur gültig, wenn das Flag **MAPI_NATIVE_BODY** in der Struktur [RTF_WCSINFO](rtf_wcsinfo.md) der _UlFlags_ -Parameter übergeben wird, die an die Funktion [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) übergeben wird. Dies kann eine der folgenden Werte sein: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper RTF weist.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper nur-Text-Format weist.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Dieser Wert wird nur verwendet, wenn _UlFlags_ das Flag **MAPI_NATIVE_BODY enthält** und der Textkörper-Format (Hypertext Markup Language weist).  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

