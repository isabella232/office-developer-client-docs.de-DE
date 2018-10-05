---
title: IConverterSessionSetCharSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385725"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass eine optional, die die MAPI zur Verwendung von MIME-Konverter Zeichensatz beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parameter

 _fApply_
  
> [in] Gibt an, ob Sie einen bestimmten Zeichensatz für die Konvertierung verwenden. Legen Sie diesen Parameter auf **true fest,** den Zeichensatz in nachfolgenden Konvertierungen anwenden. Legen Sie diesen Parameter auf **false festgelegt** , wenn Sie nicht mehr gelten bestimmten Zeichensatz und auf die Standardwerte für nachfolgende Nachrichten zurückgeben möchten. 
    
 _hcharset_
  
> [in] Ein Handle für einen Zeichensatz gemäß Definition im mimeole.h von Windows Mail. Geben Sie **null,** um anzugeben, dass keine bestimmten Zeichensatz anwenden möchten. Für nicht - **null** -Werte können mit einer Funktion wie [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) einen Handle für den Zeichensatz abrufen. 
    
 _csetapplytype_
  
> [in] Gibt an, wie anwenden ein Zeichensatzes auf eine Nachricht zu konvertieren, gemäß Definition im mimeole.h von Windows Mail.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Funktionsaufruf ist erfolgreich.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

