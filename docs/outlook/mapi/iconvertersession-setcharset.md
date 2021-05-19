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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336659"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen optionalen Zeichensatz an, den der MAPI-zu-MIME-Konverter beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream verwendet.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parameter

 _fApply_
  
> [in] Gibt an, ob ein bestimmter Zeichensatz für die Konvertierung verwendet werden soll. Legen Sie diesen Parameter auf **true,** um den Zeichensatz in nachfolgenden Konvertierungen anzuwenden. Legen Sie diesen Parameter auf **false,** wenn Sie keinen bestimmten Zeichensatz mehr anwenden und zu den Standardwerten für nachfolgende Nachrichten zurückkehren möchten. 
    
 _hcharset_
  
> [in] Ein Handle zu einem Zeichensatz, wie in mimeole.h von Windows® Mail. Geben **Sie null** an, um anzugeben, dass Sie keinen bestimmten Zeichensatz anwenden möchten. Verwenden Sie für **Nicht-Null-Werte** eine Funktion wie [MimeOleGetCodePageCharset,](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) um ein Handle für den Zeichensatz zu erhalten. 
    
 _csetapplytype_
  
> [in] Gibt an, wie ein Zeichensatz angewendet wird, um eine Nachricht zu konvertieren, wie in mimeole.h of Windows® Mail.
    
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

