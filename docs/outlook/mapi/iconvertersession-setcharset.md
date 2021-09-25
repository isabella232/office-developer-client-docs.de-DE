---
title: IConverterSessionSetCharSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b951eeb555f800d1e625e68806ba6b19352410b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616831"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen optionalen Zeichensatz an, den der MAPI-in-MIME-Konverter verwendet, wenn eine MAPI-Nachricht in einen MIME-Stream konvertiert wird.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parameter

 _fApply_
  
> [in] Gibt an, ob ein bestimmter Zeichensatz für die Konvertierung verwendet werden soll. Legen Sie diesen Parameter auf **"true"** fest, um den Zeichensatz in nachfolgenden Konvertierungen anzuwenden. Legen Sie diesen Parameter auf **"false"** fest, wenn Sie keinen bestimmten Zeichensatz mehr anwenden und zu den Standardwerten für nachfolgende Nachrichten zurückkehren möchten. 
    
 _hcharset_
  
> [in] Ein Handle für einen Zeichensatz, wie in mimeole.h von Windows Mail definiert. Geben Sie **NULL** an, um anzugeben, dass Sie keinen bestimmten Zeichensatz anwenden möchten. Verwenden Sie für **Nicht-NULL-Werte** eine Funktion wie [MimeOleGetCodePageCharset,](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) um ein Handle für den Zeichensatz abzurufen. 
    
 _csetapplytype_
  
> [in] Gibt an, wie ein Zeichensatz zum Konvertieren einer Nachricht angewendet wird, wie in mimeole.h von Windows Mail definiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Funktionsaufruf ist erfolgreich.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

