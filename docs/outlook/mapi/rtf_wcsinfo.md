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
# <a name="rtf_wcsinfo"></a>RTF_WCSINFO

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mit dieser Struktur können Sie Informationen zum Dekomprimieren des Nachrichtentexts im komprimierten Rich Text Format (RTF) angeben und optional den Textdatenstrom im systemeigenen Format zurückgeben.
  
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
  
> Die Größe der **RTF_WCSINFO** in der Anzahl der Bytes. 
    
 _ulFlags_
  
> Dies ist die Bitmaske der Optionskennzeichen für die [WrapCompressedRTFStreamEx-Funktion.](wrapcompressedrtfstreamex.md) Die unterstützten Optionskennzeichen sind: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Dies gibt an, ob der Client die zurückgegebene umschlossene Streamschnittstelle schreiben möchte.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Dies gibt an, ob der dekomprimierte RTF in den Datenstrom geschrieben werden soll, auf den der  _lpCompressedRTFStream-Zeiger_ der [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) verweist.  <br/> |
|MAPI_NATIVE_BODY  <br/> |Dies gibt an, ob der dekomprimierte Datenstrom auch in den systemeigenen Textkörper konvertiert wird, bevor der Datenstrom zurückgibt. Dieses Flag kann nicht mit dem MAPI_MODIFY **kombiniert** werden.  <br/> |
   
 _ulInCodePage_
  
> Dies ist der Codeseitenwert der Nachricht. In der Regel wird dieser Wert aus der [kanonischen Eigenschaft PidTagInternetCodepage für](pidtaginternetcodepage-canonical-property.md) die Nachricht bezogen. Dieser Wert wird nur verwendet, wenn **das MAPI_NATIVE_BODY** in _ulFlags übergeben wird._ Andernfalls wird dieser Wert ignoriert.
    
 _ulOutCodePage_
  
> Dies ist der Codeseitenwert des zurückgegebenen dekomprimierten Datenstroms, den Sie möchten. Wenn dies auf einen Nicht-Null-Wert festgelegt ist, konvertiert die [WrapCompressedRTFStreamEx-Funktion](wrapcompressedrtfstreamex.md) den Datenstrom in die angegebene Codeseite. Wenn dieser Wert auf null festgelegt ist, entscheidet MAPI, welche Codeseite verwendet werden soll. Dieser Wert wird nur verwendet, wenn **das MAPI_NATIVE_BODY** in  _ulFlags_ übergeben wird und das Textformat nicht RTF ist. Andernfalls wird dieser Wert ignoriert.
    
## <a name="see-also"></a>Siehe auch



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

