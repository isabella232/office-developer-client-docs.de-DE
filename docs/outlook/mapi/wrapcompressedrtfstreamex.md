---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e312388a86e4b93806a7d2884884c90f570fa03e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590870"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dekomprimiert den Textkörper einer E-Mail-Nachricht im komprimierten Rich-Text-Format (RTF), gibt das Format des dekomprimierten Streams an, konvertiert optional den dekomprimierten Stream in das systemeigene Format und gibt entweder den dekomprimierten oder den konvertierten nativen Stream zurück.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Parameter

_lpCompressedRTFStream_
  
> [in] Dies ist ein Zeiger auf einen Datenstrom, der in der [kanonischen PidTagRtfCompressed-Eigenschaft](pidtagrtfcompressed-canonical-property.md) einer Nachricht geöffnet wird. 
    
_pWCSInfo_
  
> [in] Dies ist ein Zeiger auf eine 
    
   [RTF_WCSINFO](rtf_wcsinfo.md) Struktur, die Optionen für die Funktion enthält. 
    
_lppUncompressedRTFStream_
  
> [out] Dies ist ein Zeiger auf die Position, an der ein Stream für das dekomprimierte RTF zurückgegeben wird. 
    
_pRetInfo_
  
> [out] Dies ist ein Zeiger auf eine [RTF_WCSRETINFO](rtf_wcsretinfo.md) Struktur, die Informationen zum Format des zurückgegebenen dekomprimierten Datenstroms enthält. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
MAPI_E_INVALID_PARAMETER 
  
- Dies wird zurückgegeben, wenn das **MAPI_NATIVE_BODY** Flag mit dem **MAPI_MODIFY** Flag im **ulFlags-Feld** der **RTF_WCSINFO** Struktur kombiniert wird, auf die  *pWCSInfo*  zeigt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

**WrapCompressedRTFStreamEx** ermöglicht es Ihnen, auf den Text einer E-Mail-Nachricht zuzugreifen, die in komprimiertem RTF gekapselt ist, indem Sie den Datenstrom dekomprimieren, den dekomprimierten Datenstrom und sein Format sowie optional den nativen Textstream zurückgeben. Der systemeigene Textdatenstrom kann in RTF, Nur-Text oder HTML vorliegen. 
  
Das Microsoft Office Outlook-Objektmodell stellt eine **Body-Eigenschaft** für **MailItem-Objekte** und eine [MailItem.BodyFormat-Eigenschaft (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) bereit, die das Format des Textkörpers angibt. Standardmäßig ruft eine Lösung, die von Outlook nicht als vertrauenswürdig eingestuft wird, die vom Outlook Security Guard generierten Sicherheitsdialogfelder auf. Die Verwendung der exportierten MAPI-Funktion **WrapCompressedRTFStreamEx** ermöglicht einer Lösung die Verwendung der MAPI anstelle des Outlook-Objektmodells und die Vermeidung dieser Sicherheitsdialogfelder. 
  
Da das **\_ MAPI-NATIVE_BODY** Flag nicht mit dem **MAPI \_ MODIFY-Flag** im **ulFlags-Feld** der **RTF \_ WCSINFO-Struktur** kombiniert werden kann, auf die von *pWCSInfo* verwiesen wird, können Sie nur im schreibgeschützten Modus auf den systemeigenen Textstrom zugreifen. Um im Lese-/Schreibmodus auf den systemeigenen Textstrom zuzugreifen, sollten Sie die **WrapCompressedRTFStream-Funktion** verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Abrufen des Textkörpers einer Nachricht in komprimierter RTF und Konvertieren in das systemeigene Format](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

