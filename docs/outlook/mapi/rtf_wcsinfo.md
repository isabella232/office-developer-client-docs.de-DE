---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5c72af72d85c40585aa6c3cc75a1aabe3bd28f7f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578774"
---
# <a name="rtf_wcsinfo"></a>RTF_WCSINFO

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mit dieser Struktur können Sie Informationen angeben, um den Textkörper einer Nachricht im komprimierten RTF-Format (Rich Text Format) zu dekomprimieren und optional den Textstrom im systemeigenen Format zurückzugeben.
  
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
  
> Die Größe der **RTF_WCSINFO** Struktur in der Anzahl der Bytes. 
    
 _ulFlags_
  
> Dies ist die Bitmaske der Optionsflags für die [WrapCompressedRTFStreamEx-Funktion.](wrapcompressedrtfstreamex.md) Die unterstützten Optionsflags sind: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Dies gibt an, ob der Client beabsichtigt, die umschlossene Streamschnittstelle zu schreiben, die zurückgegeben wird.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Dies gibt an, ob das dekomprimierte RTF in den Stream geschrieben werden soll, auf den der  _lpCompressedRTFStream-Zeiger_ der [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) verweist.  <br/> |
|MAPI_NATIVE_BODY  <br/> |Dies gibt an, ob der dekomprimierte Datenstrom auch in den systemeigenen Textkörper konvertiert wird, bevor der Datenstrom zurückgegeben wird. Dieses Flag kann nicht mit dem **MAPI_MODIFY** Flag kombiniert werden.  <br/> |
   
 _ulInCodePage_
  
> Dies ist der Codepagewert der Nachricht. In der Regel wird dieser Wert aus der [kanonischen PidTagInternetCodepage-Eigenschaft](pidtaginternetcodepage-canonical-property.md) der Nachricht abgerufen. Dieser Wert wird nur verwendet, wenn das **MAPI_NATIVE_BODY** Flag in  _ulFlags_ übergeben wird. Andernfalls wird dieser Wert ignoriert.
    
 _ulOutCodePage_
  
> Dies ist der Codepagewert des zurückgegebenen dekomprimierten Datenstroms, den Sie benötigen. Wenn dieser Wert auf einen Wert ungleich Null festgelegt ist, konvertiert die [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) den Datenstrom in die angegebene Codepage. Wenn dieser Wert auf einen Nullwert festgelegt ist, entscheidet MAPI, welche Codeseite verwendet werden soll. Dieser Wert wird nur verwendet, wenn das **MAPI_NATIVE_BODY-Flag** in  _ulFlags_ übergeben wird und das Textkörperformat nicht RTF ist. Andernfalls wird dieser Wert ignoriert.
    
## <a name="see-also"></a>Siehe auch



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

