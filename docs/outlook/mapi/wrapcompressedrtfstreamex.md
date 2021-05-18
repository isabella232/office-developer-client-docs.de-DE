---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325774"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dekomprimiert den Textkörper einer E-Mail-Nachricht im komprimierten Rich Text Format (RTF), gibt das Format des dekomprimierten Datenstroms an, konvertiert optional den dekomprimierten Datenstrom in sein systemeigenes Format und gibt entweder den dekomprimierten Datenstrom oder den konvertierten systemeigenen Datenstrom zurück.
  
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
  
> [in] Dies ist ein Zeiger auf einen Datenstrom, der in der [kanonischen Eigenschaft PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) einer Nachricht geöffnet wird. 
    
_pWCSInfo_
  
> [in] Dies ist ein Zeiger auf eine 
    
   [RTF_WCSINFO,](rtf_wcsinfo.md) die Optionen für die Funktion enthält. 
    
_lppUncompressedRTFStream_
  
> [out] Dies ist ein Zeiger auf den Speicherort, an dem ein Datenstrom für die dekomprimierte RTF zurückgegeben wird. 
    
_pRetInfo_
  
> [out] Dies ist ein Zeiger auf [eine RTF_WCSRETINFO,](rtf_wcsretinfo.md) die Informationen zum Format des zurückgegebenen dekomprimierten Datenstroms enthält. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
MAPI_E_INVALID_PARAMETER 
  
- Dies wird zurückgegeben, wenn **das MAPI_NATIVE_BODY-Flag** mit dem **flag MAPI_MODIFY** im **ulFlags-Feld** der **RTF_WCSINFO-Struktur** kombiniert wird, auf die von *pWCSInfo verwiesen wird.* 
    
## <a name="remarks"></a>Hinweise

**Mit WrapCompressedRTFStreamEx** können Sie auf den Textkörper einer E-Mail-Nachricht zugreifen, die in komprimiertem RTF gekapselt ist, indem Sie den Datenstrom dekomprimieren, den dekomprimierten Datenstrom und dessen Format sowie optional den systemeigenen Textdatenstrom zurückgibt. Der systemeigene Textdatenstrom kann in RTF, Nur-Text oder HTML enthalten sein. 
  
Das Microsoft Office Outlook-Objektmodell stellt eine **Body-Eigenschaft** für **MailItem-Objekte** und eine [MailItem.BodyFormat-Eigenschaft (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) zur Verfügung, die das Format des Textkörpers angibt. Eine Lösung, die von Outlook nicht als vertrauenswürdig eingestuft wird, ruft standardmäßig sicherheitsdialogfelder auf, die von Outlook Security Guard generiert werden. Mithilfe der exportierten MAPI-Funktion **WrapCompressedRTFStreamEx** kann eine Lösung MAPI anstelle des Outlook-Objektmodells verwenden und diese Sicherheitsdialogfelder vermeiden. 
  
Da das **\_ MAPI-NATIVE_BODY-Flag** nicht mit dem **MAPI \_ MODIFY-Flag** im **ulFlags-Feld** der **RTF \_ WCSINFO-Struktur** kombiniert werden kann, auf die *pWCSInfo* verweist, können Sie nur im schreibgeschützten Modus auf den systemeigenen Textdatenstrom zugreifen. Zum Zugreifen auf den systemeigenen Textdatenstrom im Lese-/Schreibmodus sollten Sie die **WrapCompressedRTFStream-Funktion** verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Abrufen des Textkörpers einer Nachricht in komprimiertem RTF und Konvertieren in das systemeigene Format](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

