---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d1862f7aeae4c4bf2d1f6d1fb249a4ce90e18e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613933"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert die Codierung, die während der Konvertierung verwendet werden soll.
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>Parameter

_et_
  
> Ein [ENCODINGTYPE-Wert.](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) Es werden nur die folgenden Werte unterstützt: 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>Rückgabewert

E_INVALIDARG
  
> Der übergebene Codierungstyp war ungültig.
    
## <a name="remarks"></a>Bemerkungen

Rufen Sie **"SetEncoding"** auf, bevor [Sie IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) zum Ausführen der Konvertierung verwenden. 
  
Verwenden Sie **SetEncoding,** um die Codierung nur für den äußersten Nachrichtentext eines E-Mail-Elements festzulegen. Microsoft Outlook 2010 und Microsoft Outlook 2013 die Codierung für einzelne Anlagen auswählen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI-Konstanten](mapi-constants.md)

