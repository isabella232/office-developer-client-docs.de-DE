---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2dd9f002401f8de52a9ad187b7e5850d47caf8a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587383"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Diese Struktur können Sie Informationen, die den Textkörper einer Nachricht in der komprimierten Rich Text Format (RTF) dekomprimieren und optional in seinem nativen Format Zurückgeben des Body-Streams angeben.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Elemente

 _size_
  
> Die Größe der Struktur **RTF_WCSINFO** als Byteanzahl angegeben. 
    
 _ulFlags_
  
> Hierbei handelt es sich um die Bitmaske der Optionsflags für die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion. Flags für die unterstützten sind: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Dies gibt an, ob der Client beabsichtigt zum Schreiben der gepackten Stream-Schnittstelle, die zurückgegeben wird.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Dies gibt an, ob die dekomprimierte RTF sollte in den Stream geschrieben werden, die mit den Zeiger _LpCompressedRTFStream_ der Funktion [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) gezeigt wird.  <br/> |
|MAPI_NATIVE_BODY  <br/> |Dies gibt an, ob der dekomprimierte Stream auch der systemeigenen Stelle konvertiert wird, vor der Rückgabe des Streams. Dieses Kennzeichen können nicht mit dem **MAPI_MODIFY** -Flag kombiniert werden.  <br/> |
   
 _ulInCodePage_
  
> Dies ist der Codepagewert der Nachricht. Dieser Wert wird in der Regel aus der [PidTagInternetCodepage kanonische-Eigenschaft](pidtaginternetcodepage-canonical-property.md) für die Nachricht abgerufen. Dieser Wert wird nur verwendet, wenn das Flag **MAPI_NATIVE_BODY** _UlFlags_übergeben wird. Andernfalls wird dieser Wert ignoriert.
    
 _ulOutCodePage_
  
> Dies ist der Codepagewert der zurückgegebenen dekomprimierten Stream-Objekts, die Sie möchten. Wenn diese auf einen Wert ungleich Null gesetzt ist, konvertiert die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion den Datenstrom in der angegebenen Codepage. Wenn dies auf einen NULL-Wert festgelegt ist, beschließt MAPI Codepage verwendet. Dieser Wert wird nur, wenn das Flag **MAPI_NATIVE_BODY** _UlFlags_übergeben wird, und das Textformat nicht RTF ist. Andernfalls wird dieser Wert ignoriert.
    
## <a name="see-also"></a>Siehe auch



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

