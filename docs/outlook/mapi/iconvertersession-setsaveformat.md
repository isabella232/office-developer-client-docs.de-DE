---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336638"
---
# <a name="iconvertersessionsetsaveformat"></a>IConverterSession::SetSaveFormat

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt das Format fest, in dem der Konverter einen MIME-Datenstrom in [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md)zurückgibt.
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a>Parameter

_mstSaveFormat_
  
> in Das Speicherformat, das für einen MIME-Datenstrom verwendet werden soll. Weitere Informationen finden Sie unter Enum-Typ [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).
    
  - **SAVE_RFC1521**: Verwenden Sie MIME, dies ist die Standardeinstellung.      
  - **SAVE_RFC822**: Verwenden Sie UUEncode.
    
## <a name="return-values"></a>Rückgabewerte

S_OK
  
> Der Anruf war erfolgreich.
    
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
- [IConverterSession::SetEncoding](iconvertersession-setencoding.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI-Konstanten](mapi-constants.md)

