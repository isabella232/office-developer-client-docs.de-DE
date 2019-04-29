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
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430532"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mit dieser Struktur können Sie Informationen zum Dekomprimieren des Textkörpers einer Nachricht im komprimierten Rich-Text-Format (RTF) angeben und optional den Body-Stream im systemeigenen Format zurückgeben.
  
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
  
> Die Größe der **RTF_WCSINFO** -Struktur in der Anzahl von Bytes. 
    
 _ulFlags_
  
> Dies ist die Bitmaske von Options Kennzeichen für die [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion. Die unterstützten Options-Flags sind: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Dies gibt an, ob der Client beabsichtigt, die eingebundene Datenstromschnittstelle zu schreiben, die zurückgegeben wird.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Dies gibt an, ob das dekomprimierte RTF-Format in den Stream geschrieben werden soll, auf den durch den _lpCompressedRTFStream_ -Zeiger der [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion verwiesen wird.  <br/> |
|MAPI_NATIVE_BODY  <br/> |Dies gibt an, ob der dekomprimierte Stream auch in den systemeigenen Text konvertiert wird, bevor der Stream zurückgegeben wird. Dieses Flag kann nicht mit dem **MAPI_MODIFY** -Flag kombiniert werden.  <br/> |
   
 _ulInCodePage_
  
> Dies ist der Codepage-Wert der Nachricht. Dieser Wert wird in der Regel von der [kanonischEn Pidtaginternetcodepage (-Eigenschaft](pidtaginternetcodepage-canonical-property.md) der Nachricht abgerufen. Dieser Wert wird nur verwendet, wenn das **MAPI_NATIVE_BODY** -Flag in _ulFlags_übergeben wird. Andernfalls wird dieser Wert ignoriert.
    
 _ulOutCodePage_
  
> Hierbei handelt es sich um den Codepage-Wert des zurückgegebenen dekomprimierten Streams, den Sie wünschen. Wenn dies auf einen Wert ungleich NULL festgelegt ist, wird der Stream von der [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) -Funktion in die angegebene Codepage konvertiert. Wenn dies auf einen Nullwert festgelegt ist, bestimmt MAPI, welche Codepage verwendet werden soll. Dieser Wert wird nur verwendet, wenn das **MAPI_NATIVE_BODY** -Flag in _ulFlags_übergeben wird, und das Body-Format nicht RTF ist. Andernfalls wird dieser Wert ignoriert.
    
## <a name="see-also"></a>Siehe auch



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

