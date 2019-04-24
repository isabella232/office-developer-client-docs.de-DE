---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325774"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dekomprimiert den Textkörper einer e-Mail-Nachricht im komprimierten Rich-Text-Format (RTF), gibt das Format des dekomprimierten Streams an, konvertiert optional den dekomprimierten Stream in das systemeigene Format und gibt entweder den dekomprimierten Stream oder den konvertierter systemeigener Stream.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |msmapi32. dll  <br/> |
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
  
> in Dies ist ein Zeiger auf einen Stream, der für die [kanonische PidTagRtfCompressed-Eigenschaft](pidtagrtfcompressed-canonical-property.md) einer Nachricht geöffnet wird. 
    
_pWCSInfo_
  
> in Dies ist ein Zeiger auf eine 
    
   [RTF_WCSINFO](rtf_wcsinfo.md) -Struktur, die Optionen für die Funktion enthält. 
    
_lppUncompressedRTFStream_
  
> Out Dies ist ein Zeiger auf den Speicherort, an dem ein Stream für das dekomprimierte RTF-Objekt zurückgegeben wird. 
    
_pRetInfo_
  
> Out Dies ist ein Zeiger auf eine [RTF_WCSRETINFO](rtf_wcsretinfo.md) -Struktur, die Informationen zum Format des zurückgegebenen dekomprimierten Streams enthält. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
MAPI_E_INVALID_PARAMETER 
  
- Dieser Wert wird zurückgegeben, wenn das **MAPI_NATIVE_BODY** -Flag mit dem **MAPI_MODIFY** -Flag im **ulFlags** -Feld der **RTF_WCSINFO** -Struktur kombiniert wird, auf die von *pWCSInfo* verwiesen wird. 
    
## <a name="remarks"></a>Bemerkungen

**WrapCompressedRTFStreamEx** ermöglicht den Zugriff auf den Textkörper einer e-Mail-Nachricht, die in komprimiertem RTF gekapselt ist, indem der Datenstrom dekomprimiert wird, der dekomprimierte Stream und sein Format sowie optional der systemeigene Textstream zurückgegeben werden. Der systemeigene Textstream kann in RTF, nur-Text oder HTML sein. 
  
Das Microsoft Office Outlook-Objektmodell stellt eine **Body** -Eigenschaft für MailItem-Objekte und eine MailItem [. BodyFormat-Eigenschaft (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) bereit, die das Format des Textkörpers angibt. **** Eine Lösung, die von Outlook nicht als vertrauenswürdig eingestuft wird, ruft Sicherheitsdialogfelder auf, die vom Outlook-Sicherheitsdienst generiert werden. Die Verwendung der exportierten MAPI-Funktion **WrapCompressedRTFStreamEx** ermöglicht es einer Lösung, MAPI anstelle des Outlook-Objektmodells zu verwenden und diese Sicherheitsdialogfelder zu vermeiden. 
  
Da das **MAPI\_-NATIVE_BODY** -Flag nicht mit dem **MAPI\_-Änderungs** Kennzeichen im **ulFlags** -Feld der **RTF\_-WCSINFO** -Struktur kombiniert werden kann, auf die von *pWCSInfo*verwiesen wird, können Sie nur auf die systemeigene Textstream im schreibgeschützten Modus. Verwenden Sie die **WrapCompressedRTFStream** -Funktion, um auf den systemeigenen Textstream im Lese-/Schreibzugriff zuzugreifen. 
  
## <a name="see-also"></a>Siehe auch

- [Abrufen des Textkörpers einer Nachricht im komprimierten RTF und konvertieren in das systemeigene Format](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

