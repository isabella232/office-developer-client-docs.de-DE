---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341300"
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
  
> Ein [EncodingType](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) -Wert. Es werden nur die folgenden Werte unterstützt: 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>Rückgabewert

E_INVALIDARG
  
> Der übergebene Codierungs war ungültig.
    
## <a name="remarks"></a>Hinweise

Rufen **** Sie setEncoding auf, bevor Sie [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) zum Ausführen der Konvertierung verwenden. 
  
Verwenden **** Sie setEncoding, um die Codierung nur für den äußersten Nachrichtentext eines e-Mail-Elements festzulegen. Microsoft Outlook 2010 und Microsoft Outlook 2013 wählen Sie die Codierung für einzelne Anlagen aus. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MfcMapi verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MfcMapi verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI-Konstanten](mapi-constants.md)

