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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382421"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert die Codierung, um bei der Umwandlung verwendet werden.
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>Parameter

_et_
  
> Ein [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) -Wert. Nur die folgenden Werte werden unterstützt: 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>Rückgabewert

E_INVALIDARG
  
> Der Typ der Codierung übergeben war ungültig.
    
## <a name="remarks"></a>Hinweise

Rufen Sie **SetEncoding** vor der Nutzung [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) Konvertierung ausführen. 
  
Verwenden Sie zum Festlegen der Codierung für eine e-Mail-Elements nur die äußerste Nachrichtentext **SetEncoding** . Microsoft Outlook 2010 und Microsoft Outlook 2013 wählen Sie die Codierung für jede einzelnen Anlagen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI-Konstanten](mapi-constants.md)

